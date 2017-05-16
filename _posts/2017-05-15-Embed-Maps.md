---
layout: post
title: Embedding maps with MapperKeeper
author: Joshua Tanner
---

A primary goal of [MapperKeeper](https://www.mapperkeeper.com) is to make it easier for you to share your maps.  In the previous tutorial, I showed you how to create your first map and share it on social media.  If you already have your own website or blog, why not add your MapperKeeper map directy on your site?  Today, let's talk about embedding maps!

## Create or Edit Existing Map

If you haven't created any maps, you will need to create one.  You can follow along with our previous tutorial, [building your first map](/MapperKeeper-Tutorial/) with MapperKeeper.  Once your map is ready, you can select the `edit` option from your map dashboard.

![Edit map option](/images/embed/edit-map.png)

## Select Share

From your map editor page click the `share` option on the bottom right.

![Share Options](/images/embed/share-options.png)

## Copy Embed Snippet

The embed snippet contains the code you will need to embed the map on your own website.  Copy the `iframe` snippet to your clipboard and paste it directly in your site's html code.

![Embed](/images/embed/embed-iframe.png)

The snippet should look like this:

```html
<iframe 
  src='https://www.mapperkeeper.com/maps/df36ae21-3bb6-4909-8b51-87d00f1c4146?mode=embed' 
  height='600px' width='100%'></iframe>
```

Feel free to adjust the `height` and `width` to best fit your own website.  In the above example, we are setting the width to 100% of the parent container, and a height of 600 pixels.

## Show Off

Now your beautiful map is proudly displayed on your site.  Feel free to lean back, throw your feet up, and admire how awesome your shiny map looks!  The best thing is, any changes made to the original map will automatically show up on your site.

Take a look at our example below.  

<iframe 
  src='https://www.mapperkeeper.com/maps/df36ae21-3bb6-4909-8b51-87d00f1c4146?mode=embed' 
  height='600px' width='100%'></iframe>
