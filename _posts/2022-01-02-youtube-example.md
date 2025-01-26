---
layout: post
title: Rcognition of embedded YouTube video
description: How to post article which include youtube.
image: https://upload.wikimedia.org/wikipedia/commons/7/72/YouTube_social_white_square_%282017%29.svg
tags: feature doc
doc_index: 101
---
Normally, YouTube generates source for embedded YouTube video like following:
```
<iframe
  src="https://www.youtube.com/embed/33pe6pnw9C8?controls=0"
  title="YouTube video player"
  frameborder="0"
  allow="accelerometer;fautoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen></iframe>
```

In this theme, when `iframe` element has `src` attribute that starts with `https://www.youtube.com/`, it is recognized as embedded YouTube video and width and height is adjusted automatically.

<iframe src="https://www.youtube.com/embed/33pe6pnw9C8?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
