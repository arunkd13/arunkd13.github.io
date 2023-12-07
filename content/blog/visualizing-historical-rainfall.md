+++
title = "Visualizing historical rainfall data"
date = 2023-03-11
updated = 2023-12-07
+++

With the limited water capacity in my well, I have to depend mostly on rainfall
for growing crops in my farm. Farmers have a rich traditional knowledge about
the rainfall patterns, but I am very new to following the weather patterns and
wanted to improve my intution. To start with I wanted to visualize the
historical daily rainfall over a few decades and internalize the seasonal
rainfall pattern over my farm.

I began with searching for a good visualization scheme for seasonal variations
and Spiral plots seemed to be a good option. I mucked around with installing and
trying to use R, but it seemed to require a bit more of initial time investment
to learn it proper before I could understand what I was doing.

Then I came across [Observable](https://observablehq.com/) which is written by
the authors of [D3.js](https://d3js.org/). I already knew about D3.js as a
good framework and decided to do my visualization with Observable. With a quick
signup using my Google account I was able to play around using the large number
of examples. I also found a spiral heatmap visualization notebook that I was
able to clone and adapt to presenting my data.

Here is the result of the visualization showing rainfall over Tindivanam from
January 2000 to February 2023. Rainfall data was taken from
[Open-Meteo](https://open-meteo.com/en/docs/historical-weather-api#latitude=12.23&longitude=79.66&start_date=2000-01-01&end_date=2023-02-28&daily=precipitation_sum&timezone=auto)

<iframe width="100%" height="1430" frameborder="0"
  src="https://observablehq.com/embed/f650972998319078?cells=chart"></iframe>

## History
* 2023-12-07: Updated rainfall data up to Dec 2023