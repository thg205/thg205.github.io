---
layout: post
title:  Assignment 2
date:   2024-03-19 18:00:00 +0100
categories: jekyll update
time-series: /assets/time-series.png
bar-chart: /assets/bar-chart.png
plotly: /assets/plotly-map.html
bokeh: /assets/crime_hour_plot.html
---
## Bar chart showing downward trend in drug related incidents
This is a bar chart that shows downward trend in drug related incidents:

![Bar-chart]({{ page.bar-chart}}){:width="100%"}

## Map plot showing the drug incident density between districts
This is a map plot:

<iframe src="{{page.plotly}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

## Interactive plot that allows for comparison between crime trends in SF
This interactive plot allows for comparison between crime trends ins SF:
<iframe src="{{page.bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>
