---
layout: post
title: "DaSH - Colour blind friendly, memory management, profiling"
author: "Tom Remenyi"
date: "2016-04-22"
published: true
status: publish
draft: false
---
 
Hi DaSHers, 

Today we had a wide ranging discussion which meandered around two main themes:  colour blind friendly figures; and good practice programming.

**Colour blind friendly figure**

Over the last few weeks, Tom has been investigating how to simplify making figures colourblind friendly. He brought a few simple solutions.  Although it is very easy to chose and set colour blind friendly colours/paletts, knowng how and where to find them is tricky depending on the platform/program you are in.  So here is a rainbow range:

hexcode|normalname|designername
---|---|---
#000000|colourblindblack|black
#999999|colourblindgrey|dustygrey
#0072B2|colourblinddarkblue|deepcerulean
#56B4E9|colourblindlightblue|pictonblue
#009E73|colourblindgreen|greenhaze
#F0E442|colourblindyellow|starship
#E69F00|colourblindorange|orangepeel
#D55E00|colourblindred|tenn
#CC79A7|colourblindpink|hopbush

One of the biggest challenges was finding a way to check how an entire image looked with a particular kind of colour blindness.  The app 'Color Oracle' (http://colororacle.org/) provided a free, simple, easy, rapid, cross platform solution. It just changes the screen colour palette temporaily, allowing a quick check.  
Here are three different checks of the original image.  

Normal vision

![imageref](/figures/colourblindfriendly/TSNDRA_normal_vision_colours.png)

Deuteranopia

![imageref](/figures/colourblindfriendly/TSNDRA_colorblind_test_1.png)

Protanopia

![imageref](/figures/colourblindfriendly/TSNDRA_colorblind_test_2.png)

Tritanopia

![imageref](/figures/colourblindfriendly/TSNDRA_colorblind_test_3.png)

**Good Practice Programming**

A number of issues were discussed around good practice programming including: script design; including tests; memory management; efficiency testing and overall profiling of code performance, debugging. Mike and Damien provided links to various resources throughout the discussion to help support the discussion.  These are:

*Colour issues* 

   End the rainbow: http://www.climate-lab-book.ac.uk/2014/end-of-the-rainbow/
   https://www.stat.auckland.ac.nz/~ihaka/downloads/DSC-Color.pdf

*R weirdness*

https://ironholds.org/projects/rbitrary/

*Speed issues*

The R Inferno http://www.burns-stat.com/documents/books/the-r-inferno/

*Testing*

Software Carpentry lesson on testing  http://katyhuff.github.io/python-testing/

testthat https://cran.r-project.org/web/packages/testthat/index.html

*Building a package with devtools*

   - adding functions
   - documenting with roxygen2
   - use_test()
   - Ctrl-SHIFT-B / T / E
   - use_readme_rmd()

*Errors and debugging*

 - debugger in RStudio https://support.rstudio.com/hc/en-us/articles/205612627-Debugging-with-RStudio
 - http://software-carpentry.org/blog/2011/03/using-a-debugger.html

*Functions in R*

 - http://adv-r.had.co.nz/Functions.html

*R's copy semantics and memory*

  - http://adv-r.had.co.nz/memory.html

*Profiling R code:*

https://github.com/rstudio/profvis 

**Next week (29 Apri)**

Intro to GIS concepts ( with Manifold and QGIS)

*Coming up*

Software package management 

Speeding up R

Form mastery


  
*When:*
Friday 22 April 2016, 0915hrs - 1015hrs

*Where:*
the ground floor Flex Room at [IMAS / ACE CRC Salamanca (‘the Waterfront’)](https://www.google.com.au/maps/place/Antarctic+Climate+%26+Ecosystems+CRC/@-42.8864995,147.3332809,17.25z/data=!4m2!3m1!1s0x0000000000000000:0x6643069d32752fb7).

