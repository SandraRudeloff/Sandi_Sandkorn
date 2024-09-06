---
title: Visualizing Large Geospatial Data with Lonboard
draft: false
tags:
---

<iframe title="Gryffindor Fireplace  | Hogwarts Common Room Music &amp; Ambience" src="https://www.youtube.com/embed/0KYIwRfGrLk?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 1.76991 / 1; width: 100%; height: 100%;"></iframe>

**Did you ever want to visualize massive amounts of spatial data interactively with Python, only to find that libraries like `folium` or `pydeck` can’t quite keep up?**

Imagine handling and visualizing Germany’s population data - consisting of around 3 million 100m x 100m polygons - with ease and efficiency. In this post, I’ll introduce you to the powerful Python library [`lonboard`](https://developmentseed.org/lonboard/). and show you how it can make this a reality.

We’ll start with an overview of `lonboard` and why it stands out from other libraries. Then, dive into the Jupyter notebook shown below to experience firsthand how lonboard turns raw census data into compelling interactive visualizations. You can download and view the hosted version of the notebook [here](https://notebooksharing.space/view/d655775674ed0c20c748a965c8cb40b9115be7d25eb41f559ef42179c537f3d0).

**How `lonboard`’s Advanced Architecture Enhances Geospatial Visualization**

`lonboard` transforms geospatial data visualization with its powerful GPU-based rendering and efficient data handling technologies. Unlike most other libraries that rely on [GeoJSON](https://geojson.org/), lonboard leverages advanced formats like [GeoArrow](https://geoarrow.org/) and [GeoParquet](https://geoparquet.org/)to ensures fast, interactive experiences even with massive datasets. For more details on how it works, explore further [here](https://developmentseed.org/lonboard/latest/how-it-works/).

**Coordinate Reference System**

Let’s quickly talk about coordinate reference systems. it's basically a way to represent our 3D world on a 2D map!

- WGS84 (World Geodetic System 1984) is the go-to CRS for most global maps. It uses latitude and longitude. In order to tell geopandas, that which system we're using, we can use the code of the European Petroleum Survey Group, the pioneers behind a standardized set of geodetic codes. They made it easy to identify and use different CRSs. For WGS84, that ID is EPSG:4326.
- for the population data the European Terrestrial Reference System 1989 (ETRS89) with the Lambert Azimuthal Equal-Area projection is used. This CRS is tailored for Europe, using meters and designed to keep distortions to a minimum over large areas—perfect for regional maps! (EPSG:3035)

[test](../scripts/Visualize Germany's Population using lonboard.md)

[[Visualize Germany's Population using lonboard]]