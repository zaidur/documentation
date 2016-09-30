---
title: WebGL vs SVG| Examples | Plotly
name: WebGL vs SVG in R
permalink: r/webgl-vs-svg/
description: How to create plots using WebGL
layout: base
language: r
page_type: example_index
has_thumbnail: true
display_as: get_request
output: 
  html_document: 
    highlight: null
    keep_md: yes
    theme: null
---



# WebGL vs SVG in R

Recent versions of the R package include the `toWebGL()` function, which converts any eligible SVG graph into a WebGL plot. With WebGL, we can render way more elements in the browser.

## WebGL with 50,000 points 


```r
library(plotly)
p <- ggplot(data = diamonds, aes(x = carat, y = price, color = cut)) +
  geom_point(alpha = 0.01)
ggplotly(p) %>% toWebGL()
```

## More examples

* [Compare SVG performance to WebGL](https://plot.ly/r/webgl-vs-svg/)
* [WebGL with 1 million points](https://plot.ly/r/webgl-vs-svg-million-points/)
* [WebGL for time series](https://plot.ly/r/webgl-vs-svg-time-series/)