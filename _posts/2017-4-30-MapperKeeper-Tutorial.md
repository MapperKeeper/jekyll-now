---
layout: post
title: Building Your First Story With MapperKeeper!
author: Joshua Tanner
---

[MapperKeeper](https://www.mapperkeeper.com) is an online platform for telling stories with maps.  It has useful tools and intuitive workflows to help you create and share your map with others.  To help you get started, we built this tutorial that walks you through each step of building [this map](https://www.mapperkeeper.com/maps/df36ae21-3bb6-4909-8b51-87d00f1c4146).

## What We're Buidling

We're building a map to show the 2018 Boston Marathon and adding a rooftop bar location for those that prefer to experience the event with a beer in hand!  These spectators need to know where to watch the race and also see the marathon route.  In this tutorial we will talk about adding GeoJSON files, linking to pictures and YouTube videos, and sharing your creation on Twitter.  

## Step 1: Linking Your Social Media Accounts

Linking your social media accounts with your MapperKeeper account lets you quickly share your creations with Twitter and Facebook.  Once linked, you can share a summary and picture of your map to social media with a single click.  On the dashboard page, **link your desired social media accounts** by clicking *link account* in the left sidebar.  This step is optional, but strongly encouraged!

![link social media accounts](/images/tutorial/link_accts.png)

## Step 2: Create a New Map

Your map dashboard will contain all of your great maps that you create.  To get started with your first map, click the **new map** button.

![create a new map](/images/tutorial/new_map.png)

## Step 3: Add Required Title and Summary

Before you can save your map, you must first add a **title** and **summary**.  The title is a clear name for your map, and the summary is *what will be posted to social media*.  After adding a title and summary, you can **click save** on the bottom right.

![title, summary, and save](/images/tutorial/create_map.png)

## Step 4: Import Some Data

You can add features to your map by either drawing (points, lines, polygons) them directly, or importing data from many open formats (GeoJSON, KML, GPX, TopoJSON, IGC, CSV).  We want to add the Boston Marathon route so that our viewers can see where the runners will be running during the race.  Instead of drawing the route, lets add it to the map from an existin GeoJSON file.

Right click on [this link](https://github.com/MapperKeeper/geojson/raw/master/data/boston_marathon.geojson) and select **save link as** and save it to your computer.  After it is saved, you can import it using the map import tools on the right toolbar, or simply click and drag the file and drop it onto your map.

![add boston marathon route](/images/tutorial/import_route.png)

## Step 5: Set Title and Description for Marathon Route

When users click on the marathon route, you want them to see a title and short description for the feature.  **Click** on the line that was added to the map to open the feature tools.  Here we can add a title and description.  The title can also be used as a link when you are writing your story (we will get to this later).

![set title](/images/tutorial/add_title.png)

## Step 6: Change the Color and Style of the Line

We can make the marathon route stand out better by changing the color and style of the line.  Click on the **third tab** for the on the feature tools to see the style options.  Change the color, width, and transparency that you want.  I will use a nice red color.

![change style](/images/tutorial/change_color.png)

## Step 6: Add a Photo and Video

Features can showcase photos and YouTube videos.  When a user clicks on your map features, they can explore the media directly in the app.  The first thing we will do is add a photo.  Click on the **last tab** to add images and videos.  

Select **add image** and add the following information:

**Image Title:** Photo Credit David Schap

**Image URL:** https://github.com/MapperKeeper/mapperkeeper.github.io/raw/master/images/tutorial/david-schap-marathon.png

![add image](/images/tutorial/add_image.png)

Lastly, select **add video** and add the following information:

**Video Title:** Video Credit POPSUGAR Fitness

**YouTube URL:** https://www.youtube.com/watch?v=AR3rEtzYFKM

![add video](/images/tutorial/add_video.png)
