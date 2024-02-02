---
title: "Experimental Feature: Google AdSense"
image: https://upload.wikimedia.org/wikipedia/commons/a/af/Google_adsense.jpg
tags: ['feature']
---

This theme includes following modules in `_includes` to use Google AdSense in websites. But features are not confirmed.

|Filename|Description|
|--------|-----------|
|`google-adsense.html`|Included in header (`head.html`) and includes AdSense items in header|
|`google-ad-block.html`|Item included in body and inserts area to render advertisement. This module is supposed to be included as sidebar.|

## How to enable and use AdSense

Please edit `_config.yml` and add following:

1. Add client ID in configuration.
    ```yml
    adsense_client_id: ca-pub-9466084318094329
    ```
1. Include `google-ad-block.html` in list of sidebar:
    ```yml
    sidebar_list: ["YOUR_SIDEBAR.html","google-adsense.html"]
    ```
