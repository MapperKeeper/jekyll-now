---
layout: post
title: Working With GeoJSON
author: Joshua Tanner
---

In this post, we are going to look at GeoJSON and how to upload your own GeoJSON files into [MapperKeeper](https://www.mapperkeeper.com).

## GeoJSON

[GeoJSON](http://geojson.org/) is a standard format for defining geographic data.  Data are written completely in JSON (JavaScript Object Notation), a `key` : `value` syntax which is very readable and easy to open and manipulate in a variety of different programming languages.  Since it is human readable, you can open any `.geojson` file in a simple text editor to modify individual features.

To get a feel for what GeoJSON looks like, below is a simple example of a single point location:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "prop1": "this is a value for prop1"
  }
}
```

You can see we are explicitly stating that the feature is a point, at a given latitude and longitude, and specifying some additional related properties.  The properties object can contain any information you want.

## MapperKeeper GeoJSON

MapperKeeper extends traditional GeoJSON with its' own specification [mapperkeeper-geojson-spec](https://github.com/MapperKeeper/mapperkeeper-geojson-spec) to include properties for defining custom styles, adding a gallery of images and videos, and other useful features.  Let's take a quick look at what makes MapperKeeper GeoJSON special.


### Popup Title and Description

A `title` is a descriptive name for a map feature.  Providing a `title` is not required, but important because it shows up in the top of the popup.  You can also provide an optional `description` property that describes your map feature in more detail, which shows up in the popup.  Below is an example of adding a title and description to GeoJSON:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "title": "Portland, OR",
    "description": "City in Oregon with great tech community"
  }
```

### Routable Address

Providing an `address` property generates a navigation link in the map popup.  When a user clicks on the link, they will have the option to generate driving directions to the location specified.

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "title": "Oregon Zoo",
    "description": "Award winning zoo in Portland, Oregon",
    "address": "4001 Southwest Canyon Road, Portland, OR 97221"
  }
```

### GeoJSON Styles in MapperKeeper

A features style defines how it will look on the map.  The style portion of our specification is adopted from Mapbox's [simplestyle-spec](https://github.com/mapbox/simplestyle-spec) which is widely understood by other platforms like [GitHub](https://help.github.com/articles/mapping-geojson-files-on-github/) and [geojson.io](http://geojson.io/).   

For example, let's look at the GeoJSON sample from above with a custom style:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "title": "Portland, OR",
    "description": "City in Oregon with great tech community"
    "marker-symbol": "rocket",
    "marker-color": "#aaccee"
  }
}
```

Now we have a point feature with a `rocket symbol` and a color of `#aaccee`!  The types of symbols can be found by looking at the available [Mapbox Maki Icons](https://www.mapbox.com/maki-icons/)

In fact, the are different properties that you can define for different types of geometries.  Below are some examples:

```js
# Point
"marker-size": "medium",
"marker-symbol": "circle",
"marker-color": "#653294",

# Line
"stroke": "#653294",
"stroke-opacity": 1.0,,
"stroke-width": 3,

# Polygon
"stroke": "#653294",
"stroke-opacity": 1.0,,
"stroke-width": 3,
"fill": "#555555",
"fill-opacity": 0.6,
```

### Adding Images and Videos

You can add a gallery of images and videos into your [MapperKeeper](https://www.mapperkeeper.com) by defining an array of media items for your `gallery` property.  An array is like a list, where you can define more than just 1 item.   Each gallery item is its' own object that can either be a `image` or `youtube` video with a title and valid URL.  If the media is not owned by you, it is good practice to credit the original author in the title field.  

Gallery items automatically show up in the popup for a user to click on and explore.  Below is an example of a feature with a gallery containing a single image and video:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "title": "Oregon Zoo",
    "description": "Award winning zoo in Portland, Oregon",
    "address": "4001 Southwest Canyon Road, Portland, OR 97221",
    "gallery": [
      {
        "type": "image",
        "url": "http://www.oregonzoo.org/sites/default/files/styles/article-full/public/H_orig_about_landing.jpg",
        "title": "Image credit www.oregonzoo.org"
      },
      {
        "type": "video",
        "url": "https://www.youtube.com/watch?v=r19F6LhzhCA",
        "title": "Snow Day at Oregon Zoo, Credit Oregonian"
      }
    ]
  }
```

### Custom Properties and Adding Links

It is important to note that you can define any custom property for your GeoJSON properties object.  Also, any URL's that you have in any property are automatically converted to proper HTML links.  For example, if you were hosting an event, and you wanted to provide a link to your meetup page:

```js
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-122.669, 45.519]
  },
  "properties": {
    "title": "Maptime PDX",
    "description": "We get together monthly to solve spatial problems."
    "marker-symbol": "rocket",
    "marker-color": "#aaccee",
    "meetup-link": "http://maptime.io/portland/"
  }
}
```

## Interactive - Upload a Custom GeoJSON File in MapperKeeper


