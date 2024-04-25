---
title: How to create an HTML iframe that can dynamically change height
author: John Lecocq
date: '2023-09-16'
slug: how-to-create-a-responsive-html-iframe-element-for-dimensionally-dynamic-contents
categories:
  - Web Apps
  - Tech
tags:
  - How to
  - RShiny
  - HTML
  - iframe
---



# How to Embed a Dynamic iframe

The excellent R team brought us Shiny, an R-focused framework for web application development. These apps may be shared with others by hosting them on a web server. Once hosted on a web server, one may simply embed their web applications into a webpage using a simple iframe!

**However, there is a problem...**

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/www/stack-up-edit.jpg" alt="Image of changing heights." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 1</strong>: Each board selection has a different height just as each selection of an application may case the app to take on a different height. We adjust to the different heights of the board with our foot placement or else we might step on an area where a board was not. Similarly, we must adjust the placement of the end of the iframe or risk losing part of an app.</p>
</div>

Shiny apps come in a variety of heights, and they can even change height depending on the app functionality. This can lead to excess white space on the webpage or the app can be cut off. Luckily, there is [javascript code available](https://www.cultureofinsights.com/post/responsive-iframes-for-shiny-apps) that allows for communication between a Shiny app and an iframe. 

# Step-by-step guide

1. Write your Shiny app.
2. Include the JS code linked to in the prior section in the Shiny app code.
3. Add the code below to the website source code.

# Code needed for the webpage

Below is sample code that one may use to embed an example app into any webpage using an iframe. This code goes into a the website source code. Keep in mind that the src for the iframe element, in this case https://invo.shinyapps.io/Search2ool/, will need to be changed to the URL of the app you are embedding. Contact me with any questions!

```r
<script type="text/javascript"
src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/3.5.16/iframeResizer.min.js">
</script>
<style>
  iframe {
    min-width: 100%;
  }
</style>
<iframe id="myIframe" 
src="https://invo.shinyapps.io/Search2ool/" 
scrolling="no" frameborder="no">
</iframe>
<script>
  iFrameResize({
    heightCalculationMethod: 'taggedElement'
  });
</script>
```

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/3.5.16/iframeResizer.min.js">
</script>
<style>
  iframe {
    min-width: 100%;
  }
</style>
<iframe id="myIframe" src="https://invo.shinyapps.io/Search2ool/" scrolling="no" frameborder="no">
</iframe>
<script>
  iFrameResize({
    heightCalculationMethod: 'taggedElement'
  });
</script>

# Credits

R team for their incredible work (https://www.r-project.org/) 

D J Bradshaw for their iframe resizing work (https://github.com/davidjbradshaw/iframe-resizer)

Culture of Insights for their blog showing an example of how to use Bradshaw's code in RShiny  (https://www.cultureofinsights.com/post/responsive-iframes-for-shiny-apps)