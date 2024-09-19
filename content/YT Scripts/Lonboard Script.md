---
title: Untitled
draft: true
tags:
---

**Intro**

Have you ever wanted to visualize massive amounts of spatial data interactively with Python, only to find that libraries like folium or pydeck just can’t keep up with the performance demands? 

In this video, I’ll introduce you to the Python library `lonboard`, which makes handling and visualizing large datasets a breeze.

**Cut to Screen Recording of a Map Visualization**
I’ll walk you through a hands-on example of visualizing Germany’s population data, consisting of 3 million polygons, with ease and efficiency. Sounds challenging? With `lonboard`, it’s quick and straightforward.

Hi, I’m Sandi, a PhD student at Kühne Logistics University in Hamburg, Germany. On this channel, I dive into interesting topics that come up during my research


**lonboard**
`lonboard` is a python library that stands out with its powerful GPU-based rendering and efficient data handling technologies. Unlike most libraries that rely on `GeoJSON` `lonboard` uses  formats like `GeoArrow` and `GeoParque` to deliver fast, interactive experiences even with massive datasets. Watch as I demonstrate how quickly lonboard handles Germany’s population data.

I’ll include a hosted version of the code below for you to download and explore on your own.

**CRS**
Let’s briefly talk about coordinate reference systems. They are different ways to map our 3D world onto a 2D surface

- The standard system used for most global maps is the *World Geodetic System of 1984*. Think of it as a way to fit the entire Earth onto a flat map. It’s based on latitude and longitude, and it is references with the EPSG-code 4326.
- The system used in the German population data is the *European Terrestrial Reference System of 1989*. It is tailored for Europe and uses meters for measurements. It is references with the EPSG-code 3035.

That’s it for today! Don’t forget to check out the notebook for a detailed hands-on example and dive deeper into lonboard’s capabilities. If you enjoyed this video, hit that like button, subscribe for more content, and leave a comment if you have any questions!

Thanks for watching, and I’ll see you in the next video!