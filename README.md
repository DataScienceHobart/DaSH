# DataScienceHobart.github.io

# Tentative calendar 

Please feel free to update this calendar, but also notify the organizers. Please don't put specifics here, just a minor note and initial will do. 

<!-- writeLines(sprintf("%s |  -  |    |    | ", seq(as.Date("2016-04-15"), length = 10, by = "1 week"))) -->

Date       | Topic | Contact | Venue |
-----------|-------|---------|-------|
2016-02-05 | open  | MS      | Flex  |  
2016-02-12 | BCCVL | JB      | CMAR  |
2016-02-19 | open  | MS      |       |
2016-02-26 |  DI   | MS      | Flex  |
2016-03-04 |  NH   | MS      | Flex  |
2016-03-11 |  PB   | MS      | Flex  |
2016-03-18 |  DF   | MS      | Flex  |
2016-03-25 |  Good Friday |  |  |
2016-04-01 |  Rsbz | MS      | Flex  |
2016-05-08 | open  | MS      | Flex  |
2016-04-15 | NK    | MS      | Flex |
2016-04-22 | GIS intro  | MS   | Flex    | 
2016-04-22 |  -  |    |    | 
2016-05-06 |  GDAL |    |    | 
2016-05-13 |   |    |    | 
2016-05-20 |  WFS/WMS  |    |    | 
2016-05-27 |  -  |    |    | 
2016-06-03 |  -  |    |    | 
2016-06-10 |  -  |    |    | 
2016-06-17 |  -  |    |    | 

Upcoming

* GIS intro - what is it, with  Manifold and QGIS
 - layers
 - drawings, objects/attributes
 - rasters and images
 - thematic formatting
 - drawing and pixel editing tools
 - projections

* GDAL - GIS workhorse toolkit
 - gdalinfo, ogrinfo
 - gdal_translate, ogr2ogr
 - relation to QGIS
 - vector data formats
 - raster data formats

* QGIS and open tools

 - web services
 - ?

* GIS in the 21C
 - leaflet
 - mapserver
 - meshes
 - WebGL
 - texture mapping
 - ?
 

## How to post

1. Clone this repo. 
2. Make your edits, say by creating a .md file in _posts/ (see below)
3. Push your edits if you have the privileges, or create a [pull request](https://help.github.com/articles/creating-a-pull-request/). 

### Simple Markdown 

The simplest method is to create a [Markdown](https://daringfireball.net/projects/markdown/) file (.md) in the _posts/ directory. 

The format of the name must follow the pattern of "YYYY-MM-DD-Title.md". 

A minimal blog post consists of the following Markdown content

```
---
layout: post
title: "DaSH whatever and ever amen"
author: "Rupert Rabbit"
date: "2816-02-05"
published: true
status: publish
draft: false
---
 
Hi DaSHers, 

Last week blah de blah blah. 

Some deets with asterisks for bold emphasis: 

*When:*
Friday 12 February 2816

*Where:*
Outer group flex station


Here is a report from [800 years ago](https://datasciencehobart.wordpress.com/2016/01/27/dash-meeting-on-27-january-latex/) 
demonstrating how to use URL links in Markdown.  

Later
```
### R Markdown 

TBD

[R Markdown](rmarkdown.rstudio.com/)

[Andy South's method](http://andysouth.github.io/blog-setup/)


