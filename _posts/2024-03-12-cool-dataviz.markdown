---
layout: post
title:  "Cool Dataviz!"
date:   2024-03-12 20:00:00 +0100
categories: jekyll update
bar-chart: /assets/count_crimes.png
bokeh: /assets/crime_hour_plot.html
---
## Writing a bit

Here I write a bit. To **bold** text in markdown you put two stars on each side (**). To make text _italic_ you put underscores on each side (_). To put text into a need `box` you put two weird apostrophes on each side (`).

## Static figure

This is a static figure:

![BarChart]({{ page.bar-chart}}){:width="100%"}

## Bokeh interactive plot

This is an interactive plot:

<iframe src="{{page.bokeh}}" width="100%" height="600px" frameborder="0">
    Sorry, your browser doesn't support iframes.
</iframe>