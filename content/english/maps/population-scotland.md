---
title: "Population Density of Scotland and the Central Belt"
meta_title: ""
description: "Population Density of Scotland and the Central Belt"
date: 2026-04-03T05:00:00Z
image: "/images/maps/scotland_pop_density.png"
categories: ["Census"]
author: "Shiela Sandoval"
tags: ["python", "choropleth"]
draft: false
---

Using the latest census data of Scotland (which, at the time of writing, is from 2022) from the National Records of Scotland (NRS), I've made a choropleth map of population density per "geographic area", or a group of postcodes designated by NRS representing either a Council or a Locality (the definitiion of an "output area" in their data is a bit complicated, so I'll just refer you to [this page](https://www.nrscotland.gov.uk/publications/scotland-s-census-2022-how-the-census-geographies-were-created/) that tries to explain it). Here, population density is defined as estimate number of persons per square kilometer.

{{< figure src="/images/maps/scotland_pop_density.png" width="65%">}}

As shown by the map above, most of the areas around the west (Highlands), to the Cairngorms, as well as the areas between the Central Belt and the borders have a very low population density. As excpected, people tend to congregate in and around the cities and along the towns along the coastline. Highly populated areas are more obvious if we zoom into the Central Belt, from Glasgow and Ayrshire to Edinburgh, as shown below.

{{< figure src="images/maps/scotland_central_pop_density.png" width="75%">}}


## Data sources

- [nrscotland.gov.uk: 2022 Census Output Area boundaries - Extent of the Realm](https://www.nrscotland.gov.uk/publications/2022-census-geography-products/)
  - [Explanatory Reference](https://www.nrscotland.gov.uk/publications/scotland-s-census-2022-how-the-census-geographies-were-created/)


## Tools used

Python libraries:
- Geopandas
- Matplotlib

### Request access to source code:

[Github repository](https://github.com/shielamms/MAPS-population_density.git)