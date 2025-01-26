---
layout: post
title: Basic elements in the "home" layout
description: Detail of index page and post lists 
tags: feature doc
doc_index: 51
---
The page that has `layout: home` in the Front Matter it will be rendered as following. Usually this style

This page describes about basic elements

## Home Content

The Home Content pane is captured from the HTML or Markdown file itself.

## Post List

The Post List pane lists up posts with images.
The images are picked from `image` tag in the Front Matter of post markdown or HTML article.

If the post article does not include `image` tag, the post list uses following default image:

![default]({{'/assets/img/no_image.jpg'|relative_url}})

In a Post List pane, maximum number of articles shown in a page is 6.
If total number of posts exceeds that, pagenation feature is used.
