---
layout: page
title: UK House Price Visualisation
description: Interactive data visualisation of the price paid for houses from 1995 to the present day creating using LeafletJS
---
The UK publishes vasts amount of open data online, to make the most of this, I wanted to use one of these large sets to visualise the price paid for houses over the UK on a map. 

To do this I downloaded the _Price Paid Data_ from the [HM Land Registry](http://landregistry.data.gov.uk). I chose to download the large single file, which incorporates all prices paid for houses in the UK from 1995 to present. As of writing, the size of this file is at 3.7GB. 

I then started to parse the file using Python, making use of the pandas, numpy, and matplotlib libraries. I first split the data in to years and months, then I procedeed to group the prices by westminster parliament constituencies as this seemed like an appropriate way to split up the UK in to roughly equal population areas. This was done by creating a simple function that took a postcode and returned the constituency.

The mean price paid in each constituency for each month was reformatted in another (much smaller) file. 

Using the reformatted smaller file, I created a small web application using LeafletJS, an open-source javascript library for plotting interactive maps. This web application used GeoJSON data (also publically available online) of the parliamentary constituencies to plot their respective boundaries on the map, and then shading their area according to their mean price paid for that month. 

This was then recalculated each month and animated using LeafletJS to visualise the differences in price paid over time. 

To make the plot more intuitive to understand a gaussian blur was used on the shading of the boundaries using CSS3 SVG filters.
