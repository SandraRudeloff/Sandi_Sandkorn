---
title: Untitled
draft: true
tags:
---

<iframe title="Gryffindor Fireplace  | Hogwarts Common Room Music &amp; Ambience" src="https://www.youtube.com/embed/0KYIwRfGrLk?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 1.76991 / 1; width: 100%; height: 100%;"></iframe>

**Intro**
Ever wanted to visualize massive amounts of spatial data interactively with Python, but found that libraries like `folium` or `pydeck` just can’t keep up with the performance demands?

In this video, I’ll show you how to handle and visualize Germany’s population data, which includes around 3 million 100m x 100m polygons, using the powerful new Python library, `lonboard`.

Hi, I’m Sandi, a PhD student at Kühne Logistics University in Hamburg, Germany. On this channel, I explore the fascinating topics that arise during my research journey, sharing insights and learning together.

We’ll start with a quick overview of lonboard and why it outperforms other libraries, followed by a hands-on example using publicly available census data from Germany.

# Lonboard and why it is so fast

Lonboard is a Python library for fast, interactive geospatial data visualization in Jupyter Notebooks. Unlike other libraries it doesn't rely on GeoJson for datahnadling but makes use of technologies like GeoArrow and GeoParquet for efficient data handling and GPU-based rendering for smooth visualization. This ensures quick and responsive handling of large datasets.

# CRS

Let’s quickly talk about coordinate reference systems. it's basically a way to represent our 3D world on a 2D map!

- WGS84 (World Geodetic System 1984) is the go-to CRS for most global maps. It uses latitude and longitude. In order to tell geopandas, that which system we're using, we can use the code of the European Petroleum Survey Group, the pioneers behind a standardized set of geodetic codes. They made it easy to identify and use different CRSs. For WGS84, that ID is EPSG:4326.
- for the population data the European Terrestrial Reference System 1989 (ETRS89) with the Lambert Azimuthal Equal-Area projection is used. This CRS is tailored for Europe, using meters and designed to keep distortions to a minimum over large areas—perfect for regional maps! (EPSG:3035)

* Show the result in the beginning and how I wanted to visualize it to get a sense of the data and whether it behaves as I expect

[[Big Geospatial visualization with lonboard and Kyle Barron]]

You can find a hosted version of the notebook here:
https://notebooksharing.space/view/d655775674ed0c20c748a965c8cb40b9115be7d25eb41f559ef42179c537f3d0
