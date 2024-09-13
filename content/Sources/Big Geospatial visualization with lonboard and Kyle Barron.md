---
title: Big Geospatial visualization with lonboard and Kyle Barron
draft: true
tags: []
---

https://www.youtube.com/watch?v=NAjabS0GTdo
there is 3 parts where you can lose a lot of performance
- load data into browser
- parse it to something that can be worked with in javascript
- parse it to rendering library like deck.gl to do the drawing


# Why so fast?
-> makes the process faster on the python side and on the javascript side and on the GPU for rendering
https://developmentseed.org/lonboard/latest/how-it-works/#how-is-it-so-fast
**Geoparque** compresses really well and is really fast to read and write
- file format
the difference to other libraries that build upon deck.gl like pydeck is that those use geojson which is slow. 
- 

Building on cutting-edge technologies like GeoArrow and GeoParquet in conjunction with GPU-based map rendering, Lonboard aims to enable visualizing large geospatial datasets interactively through a simple interface.
https://geoparquet.org/
https://geoarrow.org/

In the video you referenced, the presenter discusses performance challenges in handling large datasets in web applications, particularly focusing on loading, parsing, and rendering data. The two libraries mentioned—Apache Parquet and Apache Arrow—are crucial for addressing these challenges.

1. Apache Parquet

	•	What It Is: Parquet is a columnar storage file format optimized for use in data analytics. It’s highly efficient for both storage and querying large datasets because it stores data in columns rather than rows, which reduces the amount of data read from disk.
	•	Usage: Parquet is typically used to store large amounts of data on disk. It compresses data efficiently, making it ideal for handling big datasets.

2. Apache Arrow

	•	What It Is: Arrow is an in-memory columnar data format that is designed for high-performance data processing. Unlike Parquet, which is optimized for storage, Arrow is optimized for in-memory computing, allowing for efficient data interchange between systems and tools without the need for serialization or deserialization.
	•	Usage: Arrow is used to handle and manipulate data in memory. It enables fast data processing and is often used in conjunction with Parquet. For example, data stored in Parquet format on disk can be loaded into memory as Arrow format for rapid processing in applications like JavaScript.

How They Work Together:

	•	Loading and Parsing: When you load data into a web application, it might be stored in Parquet format. To efficiently process and visualize this data in the browser, you can load it into Arrow format. Arrow’s in-memory format allows for quick access and manipulation of data, significantly improving performance when parsing the data in JavaScript.
	•	Rendering with Libraries like deck.gl: Once the data is in the Arrow format, it can be passed to a rendering library like deck.gl for visualization. The efficiency of Arrow ensures that the data is handled in a way that minimizes the performance loss during rendering.

These libraries are essential for modern web applications that deal with large datasets, ensuring that data loading, parsing, and rendering are as efficient as possible.


1. take data from geopandas
2. convert it to geoarrow and geoparquet
3. sent that to the browser
4. parse the parquet
5. put the data into the GPU for rendering

lonboard has to fit in GPU memory