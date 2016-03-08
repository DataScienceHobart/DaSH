---
layout: post
title: "Comparison of Languages"
author: "Michael Sumner"
date: "18/12/2015"
published: true
status: publish
draft: false
tags: R 
---
 

 
## R
 

{% highlight r %}
library(raadtools)
{% endhighlight %}



{% highlight text %}
## Error in library(raadtools): there is no package called 'raadtools'
{% endhighlight %}



{% highlight r %}
x <- chlafiles(product = "johnson")
{% endhighlight %}



{% highlight text %}
## Error in eval(expr, envir, enclos): could not find function "chlafiles"
{% endhighlight %}



{% highlight r %}
files <- subset(x, date > as.POSIXct("2012-04-30"))
{% endhighlight %}



{% highlight text %}
## Error in subset(x, date > as.POSIXct("2012-04-30")): object 'x' not found
{% endhighlight %}



{% highlight r %}
chla <- stack(files$fullname, varname = "chlorophyll", quick = TRUE)
{% endhighlight %}



{% highlight text %}
## Error in files$fullname: $ operator is invalid for atomic vectors
{% endhighlight %}



{% highlight r %}
mchla <- calc(chla, mean, na.rm = TRUE)
{% endhighlight %}



{% highlight text %}
## Error in eval(expr, envir, enclos): could not find function "calc"
{% endhighlight %}



{% highlight r %}
pal <- palr::chlPal(palette = TRUE)
plot(mchla, col = pal$cols, breaks = pal$breaks, legend = FALSE)
{% endhighlight %}



{% highlight text %}
## Error in plot(mchla, col = pal$cols, breaks = pal$breaks, legend = FALSE): object 'mchla' not found
{% endhighlight %}



{% highlight r %}
## GDAL bindings
library(rgdal)
{% endhighlight %}



{% highlight text %}
## Loading required package: sp
{% endhighlight %}



{% highlight text %}
## rgdal: version: 1.1-3, (SVN revision 594)
##  Geospatial Data Abstraction Library extensions to R successfully loaded
##  Loaded GDAL runtime: GDAL 2.0.1, released 2015/09/15
##  Path to GDAL shared files: C:/inst/R/R/library/rgdal/gdal
##  GDAL does not use iconv for recoding strings.
##  Loaded PROJ.4 runtime: Rel. 4.9.1, 04 March 2015, [PJ_VERSION: 491]
##  Path to PROJ.4 shared files: C:/inst/R/R/library/rgdal/proj
##  Linking to sp version: 1.2-1
{% endhighlight %}



{% highlight r %}
prj <- "+proj=laea +lon_0=147 +ellps=WGS84 +lat_0=-90"
 
map <- projectRaster(mchla, crs = prj)
{% endhighlight %}



{% highlight text %}
## Error in eval(expr, envir, enclos): could not find function "projectRaster"
{% endhighlight %}



{% highlight r %}
par(mar = c(0, 0, 0, 0))
plot(map, col = pal$cols, breaks = pal$breaks, legend = FALSE, axes = FALSE)
{% endhighlight %}



{% highlight text %}
## Error in plot(map, col = pal$cols, breaks = pal$breaks, legend = FALSE, : object 'map' not found
{% endhighlight %}



{% highlight r %}
#box(col = "white", lwd = 2)
 
cm <- spTransform(coastmap("world"), prj)
{% endhighlight %}



{% highlight text %}
## Error in spTransform(coastmap("world"), prj): could not find function "coastmap"
{% endhighlight %}



{% highlight r %}
plot(cm, add = TRUE, border = NA, col = rgb(0, 0, 0, 0.2))
{% endhighlight %}



{% highlight text %}
## Error in plot.xy(xy.coords(x, y), type = type, ...): plot.new has not been called yet
{% endhighlight %}



{% highlight r %}
library(graticule)
{% endhighlight %}



{% highlight text %}
## Error in library(graticule): there is no package called 'graticule'
{% endhighlight %}



{% highlight r %}
g <- graticule(seq(-180, 165, by = 15), 
               seq(-85, 80, by = 15),
               ylim = c(-85, 80), 
               xlim = c(-180, 180), proj = prj)
{% endhighlight %}



{% highlight text %}
## Error in eval(expr, envir, enclos): could not find function "graticule"
{% endhighlight %}



{% highlight r %}
labs <- graticule_labels(seq(-180, 150, by = 30), 
                         seq(-85, 50, by = 15),
                         xline = 0, yline = -35, proj = prj   )
{% endhighlight %}



{% highlight text %}
## Error in eval(expr, envir, enclos): could not find function "graticule_labels"
{% endhighlight %}



{% highlight r %}
plot(g, add = TRUE, lty = 3, col = rgb(0, 0, 0, 0.6))
{% endhighlight %}



{% highlight text %}
## Error in plot(g, add = TRUE, lty = 3, col = rgb(0, 0, 0, 0.6)): object 'g' not found
{% endhighlight %}



{% highlight r %}
text(labs, cex = 0.8, lab = parse(text = labs$lab), col = rgb(0, 0, 0, 0.6))
{% endhighlight %}



{% highlight text %}
## Error in text(labs, cex = 0.8, lab = parse(text = labs$lab), col = rgb(0, : object 'labs' not found
{% endhighlight %}
