---
layout: post
title: Working With GeoJSON
author: Joshua Tanner
---

In this tutorial, we are going to create a custom GeoJSON file for [MapperKeeper](https://www.mapperkeeper.com), define custom styles, and even add a gallery with a photo and video!

## GeoJSON
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

## GeoJSON Styles in MapperKeeper

MapperKeeper extends traditional GeoJSON with its' own specification [mapperkeeper-geojson-spec](https://github.com/MapperKeeper/mapperkeeper-geojson-spec) to include properties for defining custom styles, or how a feature will look on the map.  The style portion of our specification were adopted from Mapbox's [simplestyle-spec](https://github.com/mapbox/simplestyle-spec) which is widely understood by other platforms like [GitHub](https://help.github.com/articles/mapping-geojson-files-on-github/) and [geojson.io](http://geojson.io/).   

For example, let's look at the GeoJSON sample from above with a custom style:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  },
  "properties": {
    "name": "Dinagat Islands",
    "marker-symbol": "rocket",
    "marker-color": "#aaccee"
  }
}
```

Now we have a point feature with a `rocket symbol` and a color of `#aaccee`!  The types of symbols can be found by looking at the available [Mapbox Maki Icons](https://www.mapbox.com/maki-icons/)

In fact, the are different properties that you can define for different types of geometries.  Below are some examples:

```js
# Point

```
