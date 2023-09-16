---
title: How to Create a Responsive HTML iframe for Dimensionally Dynamic
  Contents
author: John Lecocq
date: '2023-09-16'
slug: how-to-create-a-responsive-html-iframe-element-for-dimensionally-dynamic-contents
categories:
  - Web App Optimization
  - Technology
tags:
  - How to
  - RShiny
  - HTML
  - iframe
---



# How to Embed an Dynamic iframe

The excellent R team brought to us Shiny, an R-focused framework for web application development. These apps may be shared with others by hosting them on a web server. One may then embed the application a webpage with a simple iframe!

However, there is an issue...

Shiny apps can dynamically change in height, So when embedding these types of apps within a iframe, the iframe will not automatically change in height along with the app. This results in a dualscrollbar effect, where a scrollbar will appear within the iframe which is embedded in a page with a scrollbar. 


# Scrollception

Luckily, this is a problem that has been encountered for, and javascript code has been written that facilitates communication between a Shiny app and an iframe. It really is quite simple. One must write some code in the Shiny app (not included here), and also write some code in the source code of the webpage where the app will be included.

# Code needed for the webpage

Below is the code needed to embed an example app into any webpage using an iframe. Keep in mind that the src for the iframe element, in this case https://invo.shinyapps.io/Search2ool/, may need to be changed depending on which app you are embedding. There are two apps:

(1) Digital Aesthetic Laser Safety Advisor (lenses) - src = https://invo.shinyapps.io/SearchTool/

(2) Digital Dental Laser Safety Advisor (loupe inserts) - src = https://invo.shinyapps.io/DentalLoupeInserts/

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