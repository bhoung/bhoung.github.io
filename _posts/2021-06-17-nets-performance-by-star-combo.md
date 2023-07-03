---
title: Nets performance by star combo
layout: post
categories:
  - posts
tags:
  - nba
  - sports
  - r markdown

output: 
#html_document
  md_document:
    variant: markdown_github+backtick_code_blocks
    preserve_yaml: true
    toc: false
    fig_retina: 2
  
---

In screencast #3, which builds on [#2 ](/nets-performance-in-games-missed/)
, I plot the Nets team performance by the combination of stars that take the court in '21 NBA regular season.

<!-- excerpt-start -->
code: <a href="https://gist.github.com/bhoung/769ea023915bc7f6802f667249b54508"> https://gist.github.com/bhoung/769ea023915bc7f6802f667249b54508 </a>

<a href="https://youtu.be/ccpVqk9KUsU"> <img src="/assets/images/sc3.jpeg" alt="drawing" width="600"/>  </a>
<!-- excerpt-end -->
<br>
<b>link to YouTube screencast #4 (2021-06-17) <a href="https://www.youtube.com/watch?v=ccpVqk9KUsU"> here </a></b> 


``` r
dfm %>% group_by(N_stars) %>% summarise(mean(diff), sd(diff), length(diff))
```

    ## # A tibble: 5 x 4
    ##   N_stars `mean(diff)` `sd(diff)` `length(diff)`
    ##     <int>        <dbl>      <dbl>          <int>
    ## 1       0        -6          17.0              4
    ## 2       1         2.44       13.8             18
    ## 3       2         7.43       12.5             35
    ## 4       3         2.93       13.1             15
    ## 5      NA        NA          NA                3

``` r
dfm %>% group_by(star_combo) %>% summarise(mean(diff), sd(diff), length(diff))
```

    ## # A tibble: 9 x 4
    ##   star_combo `mean(diff)` `sd(diff)` `length(diff)`
    ##   <chr>             <dbl>      <dbl>          <int>
    ## 1 ""               -6          17.0               4
    ## 2 "D"              19.7         9.29              3
    ## 3 "H"              -2.83       12.0               6
    ## 4 "HD"              1.8         8.53              5
    ## 5 "I"               0.222      12.6               9
    ## 6 "ID"              6.75       13.0              12
    ## 7 "IH"              9.44       13.0              18
    ## 8 "IHD"             2.93       13.1              15
    ## 9  <NA>            NA          NA                 3

``` r
dfm %>% ggplot(.) + geom_point(aes(y=diff, x=date)) + facet_wrap(. ~ star_combo) + geom_smooth(aes(x=date, y=diff)) + theme_cowplot()
```

<img src="/assets/images/2021-06-17-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-10-2.png" width="672" />

``` r
dfm %>% ggplot(.) + geom_histogram(aes(x=diff, fill=star_combo), binwidth = 5) + facet_wrap(. ~ star_combo) + theme_cowplot() + labs(x="margin", y="#games")
```

<img src="/assets/images/2021-06-17-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-11-1.png" width="672" />

``` r
dfm %>% ggplot(.) + geom_density(aes(x=diff, fill=star_combo), binwidth = 5) + facet_wrap(. ~ star_combo) + theme_cowplot() + labs(x="margin", y="#games", fill="Star Combo")
```

<img src="/assets/images/2021-06-17-nba-21-bbr_files/figure-markdown_github/unnamed-chunk-12-1.png" width="672" />
