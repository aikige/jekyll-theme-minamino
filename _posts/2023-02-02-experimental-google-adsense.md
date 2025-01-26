---
title: Post Sidebar - Google AdSense (Experimental)
image: https://upload.wikimedia.org/wikipedia/commons/a/af/Google_adsense.jpg
tags: feature
---

This theme includes following modules in `_includes` to use Google AdSense in websites. But features are not confirmed.

|Filename|Description|
|--------|-----------|
|`google-adsense.html`|Included in header (`head.html`) and includes AdSense items in header|
|`google-ad-block.html`|Item included in body and inserts area to render advertisement. This module is included in *page* and *post* layout if AdSense is enabled. And it is also possible to included this as a sidebar.|

## How to enable and use AdSense

Please edit `_config.yml` and add following:

1. Add client ID in configuration.
   This will enable AdSense and `google-ad-block.html` will be included in *page* and *post* layouts.
    ```yml
    adsense_client_id: ca-pub-9466084318094329
    ```
1. (Optional) include `google-ad-block.html` in list of sidebar:
    ```yml
    sidebar_list: ["YOUR_SIDEBAR.html","google-adsense.html"]
    ```
