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
oldest_houses: /assets/oldest_houses.html
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

Now let's compare the price trends. Here, we have calculated a standardized price per municipality to be able to compare them to each other. Chart below is interactive! Please have some fun clicking on different municipalities.

<iframe src="{{page.price_trend_mun_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Here we see that most of them follow the same price trends, but there seem to be differentiating the most in the most recent years.

Another question might arise, if there are some different price trends when looking at the type of property: **Apartment**, **Plexi/Semi house** and **Private house**. I wouldn't have called it, but all the trends seem to be following the same path. 

<iframe src="{{page.price_trend_prop_type_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Now again looking at Iceland as a whole, we see what regions are the most expensive, both in regards of purchase price of property and the square meter price. By hovering ower the graph with your cursor, your able to gain more informations per region!

<iframe src="{{page.avg_price_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

<iframe src="{{page.avg_price_per_m2_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

**It's apparent:** The capital region is both the most expensive via purchase price and the square meter price. Also, true for other regions, the graphs do not change, meaning both pruchase price and square meter price are similar per region.

### Zooming in: The Capital Region of Iceland
Most people live in Reykjavík or close by municipalities. Therefor, the most interesting thing to investigate would be via postal code, that is, the postal codes that are associated with "The Capital Region of Iceland". The prices are often heavily influenced by postal code.

Take a look at the most expensive postal codes in this fun and interactive map:

<iframe src="{{page.avg_price_folium}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

**Interesting insights:**
* Postal code 111 is by far the cheapest one, average price of 31.16 mISK which is approximately 1.5 mDKK
* But perhaps surprising postal code 102 is the most expensive, average price of 67.34 mISK or approximately 3.37 mDKK
* Also, even though 270 (Mosfellsbær) is the furthest away from the city center of Reykjavík, then it's still sitting at the middle of the bunch 

Next plot is for the business savvy - always wanting to make the big bucks - **Presenting:** Historical "best buys" where we have calculated the percentage change since the property was bought, comparing purchase price to current property value - the value that indicates what you could most likely get for your apartment when putting it up for sale. Please, try out our filter, so you can get a feeling for the different sizes based on property types.

Flott mynd 4:
<iframe src="{{page.hist_best_buys}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

And finally, who doesn't want to live in a big mansion, with hundreds of square meters. We got the answer for you. But what about those that are less materalistic? Don't worry, we also got you covered...also pointing out the smallest properties sold. Please, try out our filter, so you can get a feeling for the different sizes based on property types.

Flott mynd 5:
<iframe src="{{page.property_size_groups}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

### For the odd ones
If you would not like to live in the hustle and bustled of Reykjavík (for an Icelandic standard at lest) then we made a little analysis for the *less social ones* of the bunch. If you dream of isolation Iceland is the place to be, and Bbelow you can see the 3 most isolated houses that where sold between 2006-2024. 

Flott mynd 3:
<iframe src="{{page.isolated_houses}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Or for the other ones that don't like all the newest and latest, than here is an interactive map showcasing the oldest houses sold between 2006-2021. If your not afraid of mold and leaky piping... move the courser over the map to get more details about each house!

Oldest houses:
<iframe src="{{page.oldest_houses}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>


