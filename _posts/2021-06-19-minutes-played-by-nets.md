---
title: Minutes played by Nets 
layout: post
categories:
  - posts
tags:
  - nba, sports, r markdown
output: 
   #html_document
  md_document:
    variant: markdown_github+backtick_code_blocks
    preserve_yaml: true
    toc: false
    fig_retina: 2
  
---

Screencast #4 shows the minutes played by Nets in NBA regular season '21 against team win/loss and margin.

<b>link to YouTube screencast #4 (2021-06-19) <a href="https://www.youtube.com/watch?v=Zdrv0gmIp90"> here <a> 
<a href="https://www.youtube.com/watch?v=Zdrv0gmIp90"> <img src="/assets/images/sc4.jpeg" alt="drawing" width="600"/>  </a>
<br>



``` r
roster <- "https://www.basketball-reference.com/teams/BRK/2021.html"

html <- read_html(roster)
tables <- html %>% html_nodes("table") %>% html_table()
df <- tables[1] %>% data.frame()

players <- html %>% html_nodes("table") %>% xml_find_all(".//a") %>% xml_attrs()
gamelogs <- unlist(players)
pgl <- gamelogs[grep("gamelog", gamelogs)]  %>% unique() %>% list() 
pgl <- pgl[[1]]

playoffs_pl <- pgl[c(1,2,3,4,6,9,10,14,12,15,18)]
```

``` r
get_player_url <- function(path) {
  paste("https://www.basketball-reference.com/",path,sep="")
}

player_urls <- unlist(lapply(FUN=get_player_url, playoffs_pl))

get_data <- function(player_url) {
  html <- read_html(player_url)
  tables <- html %>% html_nodes("table") %>% html_table()
  df <- tables[8] %>% data.frame()
  return(df)
}
```

``` r
for (p in player_urls) {
   pname <- str_split(p, "/")[[1]][7]
   data <- get_data(p)
   assign(pname, data) 
}
```

``` r
plist <- list()
for (p in player_urls) {
   pname <- str_split(p, "/")[[1]][7]
   plist <- c(plist, pname)   # Add element to list
}
unlist(plist)
```

    ##  [1] "hardeja01" "irvinky01" "duranke01" "harrijo01" "greenje02" "shamela01"
    ##  [7] "brownbr01" "claxtni01" "griffbl01" "jamesmi02" "johnsty01"

``` r
i = 1
for (p in plist) {
  
  if (i == 1) {
      data = get(p)
      data$player <- p
        
  } else {
      df = get(p)
      df$player <- p
      data = rbind(data, df) 
  }
  i = i + 1
}
```

``` r
table(data$player)
```

    ## 
    ## brownbr01 claxtni01 duranke01 greenje02 griffbl01 hardeja01 harrijo01 irvinky01 
    ##        75        75        75        75        74        71        75        75 
    ## jamesmi02 johnsty01 shamela01 
    ##        13        75        75

``` r
data$date <- as.Date(data$Date, format="%Y-%m-%d")
dfm <- games %>% left_join(data, by=c("date"="date"))

mp <- dfm %>% select(date, MP, player, WinLoss, diff)
mp$min <- as.difftime(mp$MP, format = "%M:%S", units = "mins")

mp %>% filter(!is.na(player)) %>% ggplot(.) + geom_point(aes(x=date, y=min, colour=player)) +
  facet_grid(WinLoss ~ .) + theme_cowplot()
```

<img src="/assets/images/2021-06-19-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-11-1.png" width="672" />

``` r
mp %>% filter(!is.na(player)) %>% ggplot(.) + geom_point(aes(x=date, y=min, colour=player)) +
  facet_grid(player ~ .) + theme_cowplot() + labs(y="minutes played")
```

<img src="/assets/images/2021-06-19-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-11-2.png" width="672" />

``` r
p1 <- mp %>% filter(!is.na(player) & WinLoss == "W") %>% ggplot(.) + geom_point(aes(x=date, y=min, colour=player)) + facet_grid(player ~ .) + theme_cowplot() + theme(legend.position = "none") + labs(y="minutes played")

p2 <- mp %>% filter(!is.na(player) & WinLoss == "L") %>% ggplot(.) + geom_point(aes(x=date, y=min, colour=player)) + facet_grid(player ~ .) + theme_cowplot() + theme(legend.position = "none") + labs(y="minutes played")


plot_grid(p1, p2)
```

<img src="/assets/images/2021-06-19-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-11-3.png" width="672" />

``` r
mp %>% filter(!is.na(player)) %>% ggplot(.) + geom_point(aes(x=date, y=min, colour=WinLoss)) + facet_grid(player ~ .) + theme_cowplot()
```

<img src="/assets/images/2021-06-19-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-11-4.png" width="672" />
