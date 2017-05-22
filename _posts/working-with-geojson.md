---
layout: post
title: Working With GeoJSON
author: Joshua Tanner
---

In this tutorial, we are going to create a custom GeoJSON file for [MapperKeeper](https://www.mapperkeeper.com), define custom styles, and even add a gallery with a photo and video!

[GeoJSON](http://geojson.org/) is a standard format for defining geographic data.  Data are written completely in JSON (JavaScript Object Notation), a `key` : `value` syntax which is very readable and easy to open and manipulate in a variety of different programming languages.  Since it is human readable, you can open any `.geojson` file in a simple text editor to modify individual features.

To get a feel for what GeoJSON looks like, below is a simple example of a single point location:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  },
  "properties": {
    "name": "Dinagat Islands"
  }
}
```

You can see we are explicitly stating that the feature is a point, at a given latitude and longitude, and specifying some additional related properties.  The properties object can contain any information you want.

