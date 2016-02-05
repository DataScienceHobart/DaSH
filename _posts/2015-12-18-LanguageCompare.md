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
## Error in plot(mchla, col = pal$cols, breaks = pal$breaks, legend = FALSE): error in evaluating the argument 'x' in selecting a method for function 'plot': Error: object 'mchla' not found
{% endhighlight %}



{% highlight r %}
## GDAL bindings
library(rgdal)
 
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
## Error in plot(map, col = pal$cols, breaks = pal$breaks, legend = FALSE, : error in evaluating the argument 'x' in selecting a method for function 'plot': Error: object 'map' not found
{% endhighlight %}



{% highlight r %}
#box(col = "white", lwd = 2)
 
cm <- spTransform(coastmap("world"), prj)
{% endhighlight %}



{% highlight text %}
## Error in spTransform(coastmap("world"), prj): error in evaluating the argument 'x' in selecting a method for function 'spTransform': Error: could not find function "coastmap"
{% endhighlight %}



{% highlight r %}
plot(cm, add = TRUE, border = NA, col = rgb(0, 0, 0, 0.2))
{% endhighlight %}



{% highlight text %}
## Error in plot.xy(xy.coords(x, y), type = type, ...): plot.new has not been called yet
{% endhighlight %}



{% highlight r %}
library(graticule)
g <- graticule(seq(-180, 165, by = 15), 
               seq(-85, 80, by = 15),
               ylim = c(-85, 80), 
               xlim = c(-180, 180), proj = prj)
labs <- graticule_labels(seq(-180, 150, by = 30), 
                         seq(-85, 50, by = 15),
                         xline = 0, yline = -35, proj = prj   )
 
plot(g, add = TRUE, lty = 3, col = rgb(0, 0, 0, 0.6))
{% endhighlight %}



{% highlight text %}
## Error in plot.xy(xy.coords(x, y), type = type, ...): plot.new has not been called yet
{% endhighlight %}



{% highlight r %}
text(labs, cex = 0.8, lab = parse(text = labs$lab), col = rgb(0, 0, 0, 0.6))
{% endhighlight %}



{% highlight text %}
## Error in text.default(x = structure(c(3210912.58979174, 5252917.77153665, : plot.new has not been called yet
{% endhighlight %}
