---
title: "Animation: Annual Surface Temperature Anomalies"
date: 2026-04-03T05:00:00Z
image: "/images/maps/global_temperature_anomaly_2025.png"
categories: ["Climate", "Polar"]
author: "Shiela Sandoval"
tags: ["python"]
draft: false
---

This project shows annual global surface temperature deviations from mean temperatures in 1951-1980.
The data comes from NASA Goddard Institute for Space Studies Surface Temperature Analysis v4. Inspired by ECMWF's plotting style in its [Copernicus Climate Change Service Atlas (C3S Atlas)](https://atlas.climate.copernicus.eu/atlas), the plots were created with XArray, Cartopy, and Matplotlib. A basic outline of the coastlines was added to make the continents more recognisable.


### Global Scale

The [Robinson projection](https://en.wikipedia.org/wiki/Robinson_projection) was used to plot the data across the mostly inhabited parts of the globe. Since distortion along the poles is severe in this projection, separate plots of the poles were made (see sections below). The goal in this plot was to visualise the warming globe from the 1980s. See how hotter temperature anomalies have become more common and more intense from the 2000s.

{{< figure src="/images/maps/temperature_anomaly_animation1.gif" width="100%">}}

{{< notice "note" >}}
There is a slight annoyance with the shifting gradients on the colourbar, even though the upper and lower limits stay the same. I've tried just setting the colourbar values to the levels in 2025 (instead of re-plotting it for every year's data), but I haven't gotten it to work.
{{< /notice >}}


### The Arctic

This plot was initially plotted with an Orthographic projection centering on 90°N and 0° longitude. However, this resulted to the Arctic region being a bit too small for the surface temperature data to be of visual significance. The North Polar Stereographic projection was instead used, with some zooming and reshaping to work around the shape of the globe when viewed from above the Arctic. The resulting image is a pseudo-orthographic view of the Arctic region from a latitude just below Iceland.

{{< figure src="/images/maps/temperature_anomaly_animation1_arctic.gif" width="70%">}}

{{< notice "note" >}}
Annoyingly the tile around the north pole is just one big awkward circle. How have others worked around the map tiles over the poles?
{{< /notice >}}


### The Antarctic

The South Polar Stereographic projection was used to plot the data over the Antarctic, using the same transformation done as the one in the Arctic plot above. This zooms into the Antarctic continent so that the surface temperature anomaly data can be more easily seen over the region.

{{< figure src="/images/maps/temperature_anomaly_animation1_antarctic.gif" width="70%">}}



## Data Sources

- **NASA Goddard Institute for Space Studies (GISS) Surface Temperature Analysis (v4)**

  [Land-Ocean Temperature Index (LOTI) deviations from the 1951-1980 means](https://data.giss.nasa.gov/gistemp/data_v4.html)

- **NaturalEarth dataset**

    [NaturalEarth data: "Admin 0 - Countries" 1:50m Cultural Vector](https://www.naturalearthdata.com/downloads/50m-cultural-vectors/): _De facto_ boundaries of countries in the world.


## Tools Used

Python libraries:
- Cartopy
- Xarray
- netCDF4
- Matplotlib

### Request access to source code

Github: https://github.com/shielamms/MAPS-climate-anomalies.git
