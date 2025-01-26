---
layout: post
title: Optional "home" Pane - Page List
description: How to show list of links beside Home pane
tags: feature doc
doc_index: 61
---
When `_config.yml` contains `home_pages` tag like following:

```
home_pages:
  - about.md
  - getting_started.md
  - doc.html
```

The `home` layout shows these pages in the sidebar of the Home pane.

When listed pages contain an `image` tag in the Front Matter, the link shows the image as its background.

## Exclusion between Embedded X pane

When Embedded X pane is enabled, `home_pages` tag is ignored.

{% include link.html path='2025-01-03-twitter-pane.md' %}
