---
title: Where was the support for the freedom friendly minor parties geographically?
layout: post
categories:
  - posts
tags:
  - australian politics
output:
  #html_document
  md_document:
    variant: markdown_github+backtick_code_blocks
    preserve_yaml: true
    toc: false
    fig_retina: 2

---

<style>
.html-widget {
    margin: auto;
}
</style>

### Background

A significant minority of Australians became politically active in the
past year, largely off the back of perceived excessive government
intervention in the form of covid lockdowns and vaccine mandates. This
was most visible from the levels of attendance of protest marches across
major cities across Australia in late 2021 into 2022, which roughly
coincided with the 6 months leading up to the federal election (just
past in late May).

While it appeared that these people would impact the results of the
election, there was little meaningful impact in actuality, in terms of
the candidates who eventually won their electorates. This is
unsurprising insofar that were dissident/disaffected voters spread
roughly evenly across geography, then the lack of concentration in each
electorate would mean that freedom friendly candidates were unlikely to
win a majority vote, even after the re-distribution of preferences.

The prominent political parties catering to disaffected voters were the
United Australia Party (the party funded by Cliver Palmer and lead by
former Liberal MP Craig Kelly), Paul Hanson’s One Nation, and the
Liberal Democratic Party, a libertarian party.

### The 2022 Australian Federal Election

The results for the lower house are in from the 2022 Australian Federal
Election. Looking at data from the Australian Electoral Commission,
there were 8,479 polling places with geographic coordinates, and 64
polling places without geographic coordinates. These polling places
collected 12,915,611 and 149,053 votes, respectively^.

^The polling places without geographic coordinates were listed as having
multiple sites.

Figure 1 below shows a histogram of the percentage of first preference
votes that went to UAP/PHON/LDP by polling place.

First preference votes for the freedom friendly minor parties (UAP, PHON
and LDP) averaged 10.3% across polling places, with a standard deviation
of 5.5%. The median polling place had 9% of votes going to the FFMPs,
while the frequency weighted mean of percentage votes going to FFMPs was
9.6%, with weighting based on total polling place votes.

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/hist-1.png" width="576" />

The top 10 polling places by support for FFMPs are shown below, where
*n_poll* is the total number of votes at the polling place, *n* are
votes for FFMPs, and the percentage supporting FFMPs are presented in
the last column.

The Glenden polling place in the Queensland electorate of Capriconia had
the greatest level of support at 41%, i.e. 32 out of 78 votes - a very
small number of votes. Note the representation by state in the top 10
polling places, as they are indicative of broader state level trends.

#### Table 1: Top 10 ranked polling places in support of FFMPs

| pollingplace             | candidate     | division    | state | n_poll | n_ffmp | ffmp (%) |
|--------------------------|---------------|-------------|-------|--------|--------|----------|
| Glenden                  | STANTON       | Capricornia | QLD   | 78     | 32     | 41       |
| Kapooka PPVC             | ORCHARD       | Riverina    | NSW   | 154    | 58     | 37       |
| Koumala                  | STANTON       | Capricornia | QLD   | 348    | 127    | 36       |
| RAAF Wagga Wagga PPVC    | ORCHARD       | Riverina    | NSW   | 173    | 64     | 36       |
| Mendooran                | VAN DER STEEN | Parkes      | NSW   | 314    | 110    | 35       |
| Kooralbyn                | HICKS         | Wright      | QLD   | 468    | 157    | 33       |
| Murrays Bridge           | McDONALD      | Maranoa     | QLD   | 150    | 50     | 33       |
| Swayneville              | STANTON       | Capricornia | QLD   | 329    | 111    | 33       |
| Perth Airport BRAND PPVC | TAYLOR        | Brand       | WA    | 65     | 22     | 33       |
| EAV Flynn PPVC           | WIEDEN        | Flynn       | QLD   | 12     | 4      | 33       |

<!-- excerpt-start -->

### The Disappointment that is Melbourne

The map of Victoria identifies polling places by levels of support for
FFMPs: ranging from 0 up to 45%. i.e. 0-5%, 5-10%, 10-15%, 15-20%,
25-35%, and 35-45%. Darker orange shading indicates greater levels of
support. Note the deliberately de-emphasized white large circles in
inner-city Melbourne, where votes of residents presumably favoured the
Greens or the Labour. The size of the markers are scaled according to
quantiles of total votes at each polling place.

Support for the FFMPs in Victoria were largely at the outer fringes of
Melbourne, predominantly the south-east of Melbourne in
Dandenong/Pakenham and the surrounding area (e.g. polling booth
Dandenong ISAACS PPVC with \~21%). There was also some support in the
north near South Morang/Thomastown (South Morang Lakes 20% & Thomastown
West 18%) and in the west near Sunshine and Hoppers Crossing (Derrimut
Health and the Grange both had 18% support).

<center>

<div class="figure">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/vic-map-1.png" alt="F2. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in Victoria at Polling Places" width="768" />
<p class="caption">
F2. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in
Victoria at Polling Places
</p>

</div>

</center>
<!-- excerpt-end -->

> ***NOTE:*** click through or download and open the
> [html](../assets/images/2022-06-11-freedom-friendly.html) version of
> this blog post to browse the results of the polling places using
> interactive maps. A
> [pdf](../assets/images/2022-06-11-freedom-friendly.pdf) version is
> also available.

Interestingly, there appeared to by quite a few pre-poll voting centres
(PPVC) with high levels of support for the freedom parties, meaning that
disaffected voters were likely to have held firm views weeks out from
the election.

Really though, the main centre of support for the FFMPs was the outpost
of Traralgon/Moe/Morwell, with support at polling places ranging between
16% and 22%. Total votes at polling places in this locale were mostly
less than a thousand, however, Morwell GIPPSLAND PPVC stood out as the
exception on voter numbers/population size with 19% FFMP support from a
total 8060 overall votes. Traralgon PPVC had similar numbers at 16% for
FFMPs from 12,804 votes.

Zooming out, there is also some concentrations of support near Mildura
and Swan to the north/north-west of the state. I say that Melbourne is
disappointing though, because really support for the freedom friendly
parties is relatively fringe, when compared with Queensland and NSW
which we will look at next.

### Signs of Resistance in Sydney, Pushback in NSW

Like Melbourne, support for the freedom friendly parties in inner-city
Sydney was lacking, fluctuating near and below 5%. Reflecting a
regional/metropolitan divide, there was similarly greater support for
UAP/PHON/LDP outside of Sydney, in the second and third most populous
cities of Wollongong and Newcastle. FFMP support hovered around 18% in
Wollongong, and as high as 17% at Singleton South polling place and as
high as 28% at Seaham, which appears to be a town adjacent to Maitland
at the outskirts of the broader Newcastle population cluster.

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/syd-map-1.png" alt="F3. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in Sydney at Polling Places" width="768" />
<p class="caption">
F3. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in
Sydney at Polling Places
</p>

</div>

The main resistance to the red & teal wave was in the
division/electorate of Werriwa, located in western Sydney. For instance,
support for the freedom friendlies ranged between 23% and 27% for the
top 10 polling places in Werriwa by support for FFMPs. Werriwa is more
encouraging than the pockets of support in Melbourne because the levels
of support are higher - approaching 25%, meaning that the contest of
ideas and popular opinion are closer to being won in that local area.
This translates to a healthier public discourse, less suppression of
‘alternative’ perspectives, and also in a practical sense is much closer
in distance to obtaining political representation, which requires a
majority vote after redistribution of preferences.

#### Table 2: Top 10 ranked polling places in Werriwa by support for FFMPs

| pollingplace                | n_poll | n_ffmp | ffmp (%) |
|-----------------------------|--------|--------|----------|
| Wetherill Park WERRIWA PPVC | 1782   | 482    | 27       |
| West Hoxton WERRIWA PPVC    | 13152  | 3484   | 26       |
| West Hoxton South           | 1286   | 328    | 25       |
| Middleton Grange            | 1316   | 342    | 25       |
| Prestons West               | 1760   | 424    | 24       |
| Horningsea Park             | 1415   | 342    | 24       |
| Cecil Hills North           | 793    | 189    | 23       |
| Liverpool (Werriwa)         | 147    | 35     | 23       |
| West Hoxton                 | 875    | 203    | 23       |
| Liverpool West (Werriwa)    | 319    | 76     | 23       |

Support for the FFMPs was stronger in NSW than in Victoria, with
additional support along the coast north of Newcastle, all the way up
through Taree, Port Macquarie, Coffs Harbour before tailing off at
Grafton; support ranged between 10% and 20%. Other concentrations of
support included Wagga Wagga, Rosewood, Young, Cowra and Parkes. The
towns/areas of Broken Hill, Lightning Ridge, Cobar and Gunnedah South
near Tamworth can also all be added to the list.

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/nsw-map-1.png" alt="F4. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in NSW at Polling Places" width="768" />
<p class="caption">
F4. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in NSW
at Polling Places
</p>

</div>

There is something interesting happening near Lismore and Byron Bay at
the upper north of NSW towards the Queensland border. At the border
where state border restrictions did impact local residents through
impeding their movement, there is support for the FFMPs. The markers at
the polling places in that area exist as part of a continuous oranged
shaded grouping of support. Further away from the border, at
Mullumbimby, Byron Bay and Lismore, support for the freedom friendly
parties reached only 12%, perhaps reflecting the lesser effects of covid
related policies rolled out and enforced by the state governments. The
floods in Lismore region perhaps unsurprisingly also played a role in
drawing votes towards parties that prioritized action on climate change.

### Go Gold Coast, You Good Thing

There is cause for optimism in the Gold Coast region, along with
Queensland in general, with the highest and most consistent levels of
support for the freedom friendly parties across the country. It is
unclear as to the cause, though the PHON and the UAP both originated in
this state. Is the economy of Queensland comprised more of agriculture
and tourism than of services and industry, unlike in the other states?
Is it a cultural phenomena where the laid-back persona is just more
generally averse to rigid rule following and suppression of civil
liberties?

Aside from a hollowed out centre of minimal FFMP support in Brisbane
(which collected 2 new green seats at the election), there is
comfortable support of the FFMPs in range of 20% to the north, south and
west of Brisbane - extending out to the Sunshine Coast, Gold Coast, and
Toowomba respectively. Geographically, all these areas are part of the
South-East Queensland population cluster.

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/qld-map-1.png" alt="F5. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in QLD at Polling Places" width="768" />
<p class="caption">
F5. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in QLD
at Polling Places
</p>

</div>

Further north along the Queensland coast, there were concentrations of
strong support in the Mackay area, but less support for the FFMPs from
Townsville and further to the north.

### the Top End: Howard Springs and Humpty Doo

Darwin and the Northern Territory also stood out as having a strong
representation of freedom friendly voters at the election. The top
ranked polling places in the NT are listed below. Howard Springs is
notable for its Covid quarantine camp - whose closure was announced in
the past few days, while Scomo provided some great marketing for Humpty
Doo by having a fish curry of Barramundi from said place on New Year’s
eve.

#### Table 3: Top ranked polling places in the NT by support for FFMPs

| pollingplace            | n_poll | n_ffmp | ffmp_perc |
|-------------------------|--------|--------|-----------|
| Tindal                  | 199    | 61     | 30        |
| Berrimah                | 231    | 67     | 29        |
| Driver                  | 919    | 262    | 28        |
| Coolalinga SOLOMON PPVC | 1517   | 419    | 27        |
| West Island PPVC        | 37     | 10     | 27        |
| Bees Creek              | 669    | 168    | 25        |
| Bakewell                | 1160   | 293    | 25        |
| Howard Springs          | 888    | 205    | 23        |
| Karama                  | 1107   | 260    | 23        |
| Humpty Doo              | 1044   | 245    | 23        |

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/nt-map-1.png" alt="F6. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in Darwin,NT at Polling Places" width="576" />
<p class="caption">
F6. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in
Darwin,NT at Polling Places
</p>

</div>

### Western Australia, South Australia and Tasmania

In terms of support for the FFMPs, Western Australia appears to be a
barren wasteland. As this appears to be somewhat atypical when compared
to the rest of Australia, I am provided with an opportunity to crack a
joke about how this pattern reflects WA’s desire to secede. This latter
trait appears to be characteristic of isolated regions like Quebec in
Canada. Of course, Perth and WA largely sailed through the first two
years of the covid pandemic until the omicron variant of covid was able
to bypass their strict border controls. Another quirk for WA in the
election was that the Liberal party performed even worse in WA than
elsewhere, which political commentators attributed the federal
government’s unwelcomed calls to open up the border towards the end of
2021.

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/rest-map-1.png" alt="F7. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) across Australia at Polling Places" width="576" />
<p class="caption">
F7. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) across
Australia at Polling Places
</p>

</div>

I know I’m being a bit harsh in knocking WA when in fact both South
Australia and Tasmania also had pretty poor support for FFMPs. I
exaggerate though, because when we zoom into Adelaide, we can see some
pockets or resistance or support, depending on where you stand.

Looking across the country, there appears to be a negative correlation
between support for FFMPs and states with temperate climate. The states
with warmer and humid weather appear to be more averse to the recent
government covid-policies. I seem to remember Jared Diamond’s ‘Guns,
Germs and Steel’ makes some commentary about the relationship between
disease and tropical climates. The pattern we observe is somewhat
counter-intuitive in that the states with temperate climates tend to be
stricter in relation to health & disease policies; is this because
although areas in tropical regions tend to have more diseases they are
actually better equiped to deal with them, without strict cultural norms
of control?

<div class="figure" style="text-align: center">

<img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/unnamed-chunk-4-1.png" alt="F8. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in Adelaide and Tasmania, at Polling Places" width="50%" /><img src="/assets/images/2022-06-11-freedom-friendly_files/figure-markdown_github/unnamed-chunk-4-2.png" alt="F8. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in Adelaide and Tasmania, at Polling Places" width="50%" />
<p class="caption">
F8. Vote (%) for Freedom Friendly Minor Parties (UAP, PHON, LDP) in
Adelaide and Tasmania, at Polling Places
</p>

</div>

### Final Comments

This blog post answered in a literal sense where the support was for the
FFMPs. I reviewed the geographic distribution of
freedom-supporting/disaffected/libertarian Australian citizens, as
indicated by their first-preference voting in support of UAP, PHON or
LDP candidates. Aggregate support for these parties was as high as
between 33% and 41% in the top ten ranked polling places, albeit all at
polling places with less than 500 votes.

Those looking for similar folk can find them in, in order of likelihood
of encounter:

1.  South-East Queensland,
2.  Western Sydney near Liverpool, along the NSW coast from Port
    Macquarie, Coffs Harbour up to Grafton, as well as many regional
    towns in NSW
3.  the outer Western, Northern and South-Eastern suburbs of Melbourne,
    as well as the Traralgon surrounds
4.  the Northern suburbs of Adelaide

With larger polling booths having percentage support for the freedom
friendly parties in the 20s, particularly in QLD, the results of the
election suggests that the major parties likely preferenced each other
rather than any of the FFMPs. An analysis of results by electorate for
the FFMPs may warrant another blog post, while a review of voting trends
over time for the freedom friendly parties would be interesting. Note
that PHON and UAP have only recently earnt the label of categorisation
as freedom friendly.

Lastly, please comment below if you found this interesting. Always
interested in receiving feedback and other ideas and interpretations.
