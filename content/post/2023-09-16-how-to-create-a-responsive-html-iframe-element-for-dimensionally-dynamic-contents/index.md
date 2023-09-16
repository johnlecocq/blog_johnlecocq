---
title: How to Create a Responsive HTML "iframe" Element for Dimensionally Dynamic
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

<div>
<h1>
Here is the title
</h1>
<p>
And this is the body of the blog
</p>
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
</div>