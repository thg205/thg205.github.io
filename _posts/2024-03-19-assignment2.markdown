---
layout: post
title:  Assignment 2
date:   2024-03-19 18:00:00 +0100
categories: jekyll update
time-series: /assets/time-series.png
bar-chart: /assets/bar-chart.png
plotly: /assets/plotly-map.html
bokeh: /assets/bokeh_plot.html
---
## A data driven short story: Downward trends in drug related incidents
Some people would argue that the world has gone for worse with more drug and crime related problems every year. That we are on our way to hell, so to speak. But is that really the case?  Well, by analysing crime data from San Francisco Police Department from 2003 to 2017, interesting trends can be found. 

The dataset is a recording of incidents, including date/time, type of incident (the crime type) and geographcial location of the incident, making it possible to analyse and present relevant insights. Thus, giving us the chance to look into the crime trends of San Francisco for a long period of time, giving us a chance to answer questions about drug related incidents and if there might be a positive outlook for the city of San Francisco. To get all the details you must keep on reading!

## Is there a trend in drug related incidents?
This is a bar chart that shows downward trend in drug related incidents:

![Bar-chart]({{ page.bar-chart1}}){:width="100%"}

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

## Conclusion

## Contribution