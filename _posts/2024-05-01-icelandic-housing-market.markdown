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
<sub><sup>This webpage is built as a part of the course Social Data Analysis and Visualization at DTU during the spring semester of 2024. For more information on the work behind the webpage we have included a [explainer_notebook](https://nbviewer.org/github/thg205/thg205.github.io/blob/master/assets/Final%20Project.ipynb)</sup></sub>
---
**Imagine this:** You're scrolling through endless homes online, picturing yourself kicking back in a rooftop jacuzzi or having backyard barbecues with the family. That's the beauty (and maybe the madness) of the housing market! It's all about finding the place that matches your vibe.

For some, it's a sleek, modern condo downtown, close to the buzz of city life. For others, it's a charming older house in the suburbs, where the kids can become jungle gym champions without ending up in a game of real-life bumper cars.

The folks behind this website understand that perfectly. When they heard Iceland (yes, Iceland, not Denmark – plot twist!) made a bunch of housing data public, they were like "Let's dive in and see what makes Iceland's housing market tick!" (Especially since they're Icelandic...).

But before we start let's take a look at the datasets that where used.

### The datasets
The main dataset that was used in this project is an open-source dataset containing property registration data for the Icelandic housing market, which was downloaded from this source: [property register](https://www.fasteignaskra.is/gogn/grunngogn-til-nidurhals). It contains information on historical purchase prices, property address, postal codes, square meters, numbner of rooms, type of hosuing, etc. To obtain geological data a supplementary dataset was needed containing latitude and longitude values for each property, and by merging these two datasets together the final dataset was created and ending being 75.4 MB in size.

The dataset contains 193.005 records of property registration with 52 columns of different data, some more relevant and useful than other. By taking a look at descriptions of these different columns we were able to identify the most important features. Here are links to the descriptions, but they are in Icelandic so google translate comes in handy: [kaupskra](https://www.fasteignaskra.is/gogn/grunngogn-til-nidurhals/kaupskra-fasteigna/eigindalysing-kaupskrar) & [stadfangaskra](https://www.fasteignaskra.is/library/Samnyttar-skrar-/Fyrirtaeki-stofnanir/Nidurhal/Sta%C3%B0fangaskr%C3%A1%20eigindal%C3%BDsing.pdf).

The final set of columns/features we chose are these (english translation of the column to the right of the back slash):
- `FAERSLUNUMER/transaction_number`: Property transaction number
- `FASTNUM/property_number`: Property identification number
- `HEIMILISFANG/adress`: Address
- `POSTNR_x/postal_code`: Postal code
- `SVEITARFELAG/municipality`: Municipality
- `THINGLYSTDAGS/notarized_date`: Date of registration of purchase agreement (notarized agreement)
- `KAUPVERD/purchase_price`: Purchase price of property, given in thousand ISK
- `FASTEIGNAMAT/property_value`: Property value/assessment at the time of the purchase agreement, given in thousand ISK
- `FASTEIGNAMAT_GILDANDI/current_property_value`: Current property value/assessment, given in thousand ISK
- `BRUNABOTAMAT_GILDANDI/insurance_payout`: Current fire compensation assessment or insurance payout if destroyed, given in thousand ISK
- `BYGGAR/year_built`: Year of construction/property built
- `EINFLM/size_square_meters`: Unit area of property
- `LOD_FLM/plot_size`: Plot size
- `LOD_FLMEIN/plot_size_units`: Plot size units (not all plots given in same units)
- `FJHERB/number_of_rooms`: Number of rooms
- `TEGUND/type`: Property type
- `ONOTHAEFUR_SAMNINGUR/unenforcable_contract`: If contract is unenforceable then 1 otherwise 0
- `N_HNIT_WGS84/latitude`: North coordinates in WGS84 latitude
- `E_HNIT_WGS84/longitude`: East coordinates in WGS84 longitude
- `FULLBUID/complete`: If the property is complete then 1 otherwise 0

To enrich our data we needed other supporting datasets. Most noticably, we had two different interest rates, **index** and **non-index**. Here is link to the data of the rates: [interest rates](https://www.sedlabanki.is/annad-efni/meginvextir-si/).


### Looking at historical trends
**Diving in:** Let's start by examining historical purchase agreements from 2006 to 2023. This graph reveals a compelling trend. We see a peak in 2007, followed by a significant dip in 2009. This decline coincides with the 2008 financial crisis, a pivotal moment impacting the global economy, including Iceland's housing market.

Moving forward, we witness a steady rise in contracts, culminating in record years around 2020/2021.  This surge likely reflects the impact of COVID-19, with many seeking new living arrangements, perhaps driven by remote work opportunities.

![Bar-chart]({{page.number-of-contracts-per-year}}){:width="100%"}

So, what's the *secret sauce* behind these market ups and downs? It boils down to those pesky mortgage interest rates (and other factors but this is much more fun to look at). These rates are like tiny dials that the Central Bank of Iceland uses to control the economy. In 2009, inflation was a runaway hamster on a wheel, so they cranked up the rates to slow things down. But by 2022/2021, the economy needed a jumpstart, so they lowered the rates again.

The graph showcases the average mortgage rates (indexed and non-indexed) alongside the number of contracts. Observe how rates climbed in 2008. Rates then dipped in 2013, followed by a period of sustained growth in the housing market, Then the top was found in 2020/2021, likely fueled by increased savings during the COVID-19 lockdowns.

![Bar-chart]({{page.number-of-contracts-per-year-with-rates}}){:width="100%"}

This exploration provides a glimpse into the dynamic relationship between mortgage interest rates and the Icelandic housing market. By examining trends, we gain valuable insights into the factors shaping this ever-evolving landscape.


### Details of properties available
In Iceland there are about 60 municipalities, but many of them are small and not as interesting, so these are the 16 biggest, most of them close to **Reykjavík**, the capital city. Let's look at the different details per municipality, where we drew some insights about what you could be expecting when buying a property in one of the municipalities.

![Bar-chart]({{page.bar-chart-statistics}}){:width="100%"}

**Interesting insights:**
* The most expensive municipalities are Garðabær and Seltjarnarnes (think of Hellerup and Frederiksberg) but the cheapest ones are Fjarðarbyggð and Ísafjarðarbær located on the East- and Westfjords - pretty far from the capital region.
* Oldest houses are in Reykjavík, no real surprise there! But maybe more interesting, for most other municipalities most properties are built from 2000, indicating that many new properties have been built the last 20 years.
* Again, we see Garðabær and Seltjarnarnes have the biggest properties on average but it's Fjarðarbyggð that has the most rooms on average, or 3.5 rooms on average. I guess they need their space there in the eastfjords!

Now let's compare the price trends. Here, we have calculated a standardized price per municipality to be able to compare them to each other. Chart below is interactive! Please have some fun clicking on different municipalities.

<iframe src="{{page.price_trend_mun_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Here we see that most of them follow the same price trends, but there seem to be differentiating the most in the most recent years.

Another question might arise, if there are some different price trends when looking at the type of property: **Apartment**, **Plex/semi/linked house** and **Private house**. I wouldn't have called it, but all the trends seem to be following the same path. 

<iframe src="{{page.price_trend_prop_type_bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Now again looking at Iceland as a whole, we see what regions are the most expensive, both in regards to purchase price of property and the square meter price. By hovering ower the graph with your cursor, you're able to gain more informations per region!

<iframe src="{{page.avg_price_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

<iframe src="{{page.avg_price_per_m2_choro}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

**It's apparent:** The capital region is both the most expensive via purchase price and the square meter price. Also, true for other regions, the graphs do not change that much, meaning both purchase price and square meter price are similar per region.


### Zooming in: The Capital Region of Iceland
Most people live in Reykjavík or close by municipalities. Therefor, the most interesting thing to investigate would be via postal code, that is, the postal codes that are associated with "The Capital Region of Iceland". The prices are often heavily influenced by postal code.

Take a look at the most (or least) expensive postal codes, with regards to the average purchase price, in this fun and interactive map where the size of the dot is determined by number of purchase agreements within that postal code:

<iframe src="{{page.avg_price_folium}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

**Interesting insights:**
* Postal code 111 is by far the cheapest one, average price of 31.16 mISK which is approximately 1.5 mDKK.
* But, perhaps surprisingly, postal code 102 is the most expensive, with average price of 67.34 mISK or approximately 3.37 mDKK.
* Also, even though 270 (Mosfellsbær) is the furthest away from the city center of Reykjavík, then it's still sitting at the middle of the bunch.

We can also look at the different postal codes with regards to the average purchase price per square meter, meaning it shows where to buy properties if you want to get the most for your buck in terms of square meters:

<iframe src="{{page.avg_price_per_m2_folium}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

**Interesting insights:**
* When looking at the average price per square meter different pattern appears, now the cheapest postal code area is 109 with average price per square meter of 332 kISK/square meter, which is around 16.5 kDKK/square meter.
* The most expensive area is still 102 with a whooping 629 kISK/square meter in average price per square meter (31.1 kDKK/square meter) and thus almost two times more expensive than in postal code 109.
* Taking everything in it seems that more suburban areas are cheaper and the more centrally located you are in Reykjavík the higher the square metere price is.

Next plot is for the business savvy - always wanting to make the big bucks - Presenting historical _"best buys"_ where we have calculated the percentage change since the property was bought, comparing purchase price to current property value - the value that indicates what you could most likely get for your apartment when putting it up for sale. Please, try out our filter, so you can get a feeling for the different sizes based on property types.

<iframe src="{{page.hist_best_buys}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

And finally, who doesn't want to live in a big mansion, with hundreds of square meters. We got the answer for you. But what about those that are less materalistic? Don't worry, we got you covered...pointing out the smallest properties sold. Please, try out our filter, so you can get a feeling for the different sizes based on property types. Either way, you can zoom in and get a direction of where the biggest/smallest properties are located in the Capital Region.

<iframe src="{{page.property_size_groups}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>


### For the "odd ones"
If you would not like to live in the hustle and bustle of Reykjavík (for an Icelandic standard at least) then we made a little analysis for the *less social ones* of the bunch. If you dream of isolation, Iceland is the place to be and below you can see the 3 most isolated houses that where sold between 2006-2024. 

<iframe src="{{page.isolated_houses}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

Or for the other ones that don't like all the newest and latest, than here is an interactive map showcasing the oldest houses sold between 2006-2021. If your not afraid of mold and leaky piping... move the courser over the map to get more details about each house!

<iframe src="{{page.oldest_houses}}" width="100%" height="400px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>