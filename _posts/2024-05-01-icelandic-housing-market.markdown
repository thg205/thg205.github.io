---
layout: post
title:  The Icelandic housing market
date:   2024-05-01 11:00:00 +0100
categories: jekyll update
number-of-contracts-per-year: /assets/number_of_contracts_per_year.png
number-of-contracts-per-year-with-rates: /assets/number_of_contracts_per_year_w_rates.png
number-of-contracts-per-mun: /assets/number_of_contracts_per_mun.png
bar-chart-statistics: /assets/bar_chart_statistics.png
price_trend_mun_bokeh: /assets/price_trend_mun.html
price_trend_prop_type_bokeh: /assets/price_trend_prop_type.html
avg_price_choro: /assets/avg_price_choro.html
avg_price_per_m2_choro: /assets/avg_price_per_m2_choro.html
avg_price_folium: /assets/avg_price_folium.html
avg_price_per_m2_folium: /assets/avg_price_per_m2_folium.html
isolated_houses: /assets/isolated_houses.html
hist_best_buys: /assets/hist_best_buys.html
property_size_groups: /assets/property_size_groups.html
---
**Imagine this:** You're scrolling through endless homes online, picturing yourself kicking back in a rooftop jacuzzi or having backyard barbecues with the family. That's the beauty (and maybe the madness) of the housing market! It's all about finding the place that matches your vibe.

For some, it's a sleek, modern condo downtown, close to the buzz of city life. For others, it's a charming older house in the suburbs, where the kids can become jungle gym champions without ending up in a game of real-life bumper cars.

The folks behind this website understand that perfectly. When they heard Iceland (yes, Iceland, not Denmark – plot twist!) made a bunch of housing data public, they were like "Let's dive in and see what makes Iceland's housing market tick!" (Especially since they're Icelandic...).

### Looking at historical trends
**Diving in:** Let's start by examining historical purchase agreements from 2006 to 2023. This graph reveals a compelling trend. We see a peak in 2007, followed by a significant dip in 2009. This decline coincides with the 2008 financial crisis, a pivotal moment impacting the global economy, including Iceland's housing market.

Moving forward, we witness a steady rise in contracts, culminating in record years around 2020/2021.  This surge likely reflects the impact of COVID-19, with many seeking new living arrangements, perhaps driven by remote work opportunities.

![Bar-chart]({{page.number-of-contracts-per-year}}){:width="100%"}

So, what's the *secret sauce* behind these market ups and downs? It boils down to those pesky mortgage interest rates (and other factors but this is much more fun to look at). These rates are like tiny dials that the Central Bank of Iceland uses to control the economy. In 2009, inflation was a runaway hamster on a wheel, so they cranked up the rates to slow things down. But by 2022/2021, the economy needed a jumpstart, so they lowered the rates again.

The graph showcases the average mortgage rates (indexed and non-indexed) alongside the number of contracts. Observe how rates climbed in 2008. Rates then dipped in 2013, followed by a period of sustained growth in the housing market, Then the top was found in 2020/2021, likely fueled by increased savings during the COVID-19 lockdowns.

Mynd af **Number of contracts per year with index rates:**

![Bar-chart]({{page.number-of-contracts-per-year-with-rates}}){:width="100%"}

This exploration provides a glimpse into the dynamic relationship between mortgage interest rates and the Icelandic housing market. By examining trends, we gain valuable insights into the factors shaping this ever-evolving landscape.

### Details of properties available
In Iceland there are about 60 municipalities, but many of them are small and not as interesting, so these are the 16 biggest, most of them close to **Reykjavík**, the capital city. Let's look at the different details per municipality, where we draw some insights about what you could be expecting when buying a property in one of the municipalities.

![Bar-chart]({{page.bar-chart-statistics}}){:width="100%"}

**Interesting insights:**
* The most expensive municipalities are Garðabær and Seltjarnarnes (think of Hellerup and Frederiksberg) but the cheapest ones are Fjarðarbyggð and Ísafjarðarbær located on the east- and westfjords - pretty far from the capital region
* Oldest houses are in Reykjavík, no real surprise there! But maybe more interesting, for most other municipalities most properties are built from 2000, indicating that many new properties have been built the last 20 years.
* Again, we see Garðabær and Seltjarnarnes have the biggest properties on average but it's Fjarðarbyggð that has the most rooms on average, or 3.5 rooms on average. I guess they need there space there in the eastfjords!

Now let's compare the price trends. Here, we have calculated a standardized price per municipality to be able to compare them to each other. Chart below is interactive! Please have some fun clicking on different municipalities

<iframe src="{{page.price_trend_mun_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Here we see that most of them follow the same price trends, but there seem to be differentiating the most in the most recent years.

Another question might arise, if there are some different price trends when looking at the type of property: **Apartment**, **Ples/semi house** and **Private house**. I wouldn't have called it, but all the trends seem to be following the same path. 

<iframe src="{{page.price_trend_prop_type_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

## 

Kúkur og piss:
<iframe src="{{page.avg_price_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Meiri kúkur og piss:
<iframe src="{{page.avg_price_per_m2_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Flott mynd 1:

<iframe src="{{page.avg_price_folium}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Flott mynd 2:
<iframe src="{{page.avg_price_per_m2_folium}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Flott mynd 3:
<iframe src="{{page.isolated_houses}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Flott mynd 4:
<iframe src="{{page.hist_best_buys}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Flott mynd 5:
<iframe src="{{page.property_size_groups}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

