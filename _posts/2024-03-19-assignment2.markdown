---
layout: post
title:  Assignment 2
date:   2024-03-19 18:00:00 +0100
categories: jekyll update
time-series: /assets/time-series.png
bar-chart: /assets/bar-chart1.png
plotly: /assets/plotly-map.html
bokeh: /assets/bokeh_plot.html
---
## A data driven short story: What are the trends in drug related incidents?
Some people would argue that the world has gone for worse with more drug and crime related problems every year, escepically in big cities world wide. But is that really the case?  Well, by analysing crime data from San Francisco Police Department from 2003 to 2017, interesting trends can be found. This story focuses on drug related incidents and wether everything is going to hell, or, if there are perhaps some positive things that can be found.

The dataset is a recording of incidents, including date/time, type of incident (the crime type) and geographcial location of the incident, making it possible to analyse and present relevant insights. This gives us the chance to look into the crime trends of San Francisco for a fairly long period of time, making it possible to shed light on questions about drug related incidents for the city of San Francisco. To get all the details you must keep on reading!

### Is there a trend in drug related incidents?
The simplest of graphs can often reveal the truth. Below bar chart shows yearly trend of drug related incidents. There's a spike in incidents between 2007-2009, possibly linked to the 2007-08 international financial crisis, where many people lost there houses. The following years show a steady decline in incidents, reaching the lowest point in 2017, which coincides with economic recovery.

![Bar-chart]({{page.bar-chart}}){:width="100%"}

### "Drug map" of San Francisco - Is the problem related to a specific area?
Another way of looking at drug related incidents is by geographical location of the incident where the question would be more on the line of: "where in San Francisco is the majority of drug related crimes?". Introducing a interactive "heat map" where we illustrate the number of drug related incidents on a map of San Francisco in years 2003 to 2017, where colors indicate number of drug incidents within districs of San Francisco.

<iframe src="{{page.plotly}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

From above map it's obvious that certain areas have more drug related incidents, and one area in particular is red glowing. If you are a native San Franciscan then it comes to no surprise that this area is Tenderloin, an area which is considered one of the most dangerous one in San Francisco, where theft, assaults and drug use is prevalent.

### Does a decrease in drug related incidents indicate a similar decline in other crimes?
Until know we have only been looking at drug related incidents. But what if we want to see if other crime types follow the same trend as the drug related crimes? To investigate this further we made a interactive timeseries plot. This plot allows us to compare different crime types to our drug related crimes, giving us a fun and interactive way of comparing crime types.

On the y-axis we have the "crime rate", which is a standardized rate, enabling us to compare crime types of different magnitudes, given the different nature of crimes as some are simply more common/frequent than other. By clicking on different crime types we can choose what crime types we want to compare to Drug/Narcotics. For example, we see an interesting trend when comparing it to Larceny/Theft, where the trends are opposite meaning that Larceny/Theft is on the uprise in recent years.

<iframe src="{{page.bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>

### Conclusion
In summary, our data driven short story sheds light on drug related crimes in San Francisco, where we are seeing a dramatic decrease in incidents and that the drug related problems are highly geographic, meaning it's dependent on geographical location. On the other hand, when compared to other crime types, this seems to be one of few exceptions, where most other crime types show an increase in crime rate in recent years. Could that be due to politcal focus on decreasing drug problems and less focus on other crime types?

## Contribution
s232411 focused on setting up the web page and adding the plots to the web page whereas s232738 focused on writing the text and deriving insights from our findings. Both team members collaborated on finalizing the report.