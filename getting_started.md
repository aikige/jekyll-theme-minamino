---
title: Getting Started
layout: page
---

## Quick Start Guide

### A. Simplest way to try the theme - copy contents of test directory

Contents of [test](https://github.com/aikige/minamino-aikido/tree/main/test) directory of the repository will give good example about usage of this theme.

1. Copy contents of [test](https://github.com/aikige/minamino-aikido/tree/main/test) to
   your working directory.
1. Edit index.html and add any message in `_post` directory.
1. If you are going to use GitHub Pages, please just commit to your repository.
   Then, you'll get rendered site.
1. Otherwise, you can try to render the image using [Docker](http://docker.io/).
    1. If you are using Windows and Docker is already installed, please
       just execute `test_remote_theme_on_docker.bat`.
    1. Then Jekyll is executed on the Docker and can access to the rendered site
       http://localhost:4000/

### B. Use theme as remote-theme (recommended)

If you have knowledge of [jekyll-remote-theme](https://github.com/benbalter/jekyll-remote-theme) feature of Jekyll, that is easiest way to try this theme.

Key configuration is:

1. Add `jekyll-remote-theme` to `plugins` setting. For example:

```yml
plugins:
  # ... your plugins.
  - jekyll-remote-theme
```

2. Add `remote_theme` setting into `_config.yml`.

```yml
remote_theme: aikige/minamino-aikido
```

### C. Clone project

Otherwise, please make clone (or fork) of this repository and edit files.

## Usage of Optional Features

This theme contains following optional features:

![Home Layout with Comment](assets/img/screenshot_1024_w_comment.png)

### Embedded Tweets

If following configuration is exist in `_config.yml`, tweet pain will be shown.

```yml
embed_tweets: yes
twitter_username: aikige
```

The tweet pain shows tweets of a user specified by `twitter_username`.

### Google AdSense

If following configuration is exist in `_config.yml`, google adsense related header will be included in the page and tries to embed advertisements.

```yml
adsense_client_id: ca-pub-9466084318094329
```

### Embedded Google Calender

If following configuration is exist in `_config.yml`, google calender of specified URL will be shown as 1st article in article list.

```yml
google_calendar_url: https://calendar.google.com/calendar/embed?showTitle=0&amp;showNav=0&amp;showDate=0&amp;showPrint=0&amp;showTabs=0&amp;showCalendars=0&amp;mode=AGENDA&amp;height=240&amp;wkst=1&amp;bgcolor=%23ffffff&amp;src=minamino.aikido%40gmail.com&amp;color=%231B887A&amp;ctz=Asia%2FTokyo
```

### Embedded Amazon Affiliates

If following configuration is exist in `_config.yml`, Amazon Affiliate box will be shown at Home Layout.

```yml
amazon_ad_urls: ['//rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=F7F7F7&IS2=1&bg1=F7F7F7&fc1=000000&lc1=0000FF&t=gachin-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=as_ss_li_til&asins=B01BLA9QRU&linkId=03a9de537bfe7813cb06917a93e674ac', '//rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=F7F7F7&IS2=1&bg1=F7F7F7&fc1=000000&lc1=0000FF&t=gachin-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=as_ss_li_til&asins=4522426887&linkId=a81bcb0f7572b5d7dee8306f0c29f832']
```

Note that this parameter is expected to be an array.

### Image Width, Caption and Floating

`image.html` provides function to control width, caption and floating for images.

#### Syntax

```{% raw %}
{% include image.html url="URL" class="CLASS" width="WIDTH" %}
{% endraw %}```

All parameters are optional.
- `URL` is recognized as relative URL for source of image.
- `CLASS` is used to control styles, `right`, `left` and `center` is predefined.
  - `right` makes image floated right.
  - `left` makes image floated left.
  - otherwise image is centered.
- `WIDTH` can be used as image width. If not specified, image is rendered with its own size (`width:auto`).

```{% raw %}
{% include image.html url="assets/img/no_image.jpg"
   description="test" width="100%" %}
{% endraw %}```
{% include image.html url="assets/img/no_image.jpg" description="test" width="100%" %}

<hr class="clear" />

```{% raw %}
{% include image.html url="assets/img/no_image.jpg"
   description="float right" class="right" width="25%" %}
{% endraw %}```
{% include image.html url="assets/img/no_image.jpg" description="float right" class="right" width="25%" %}

And sample text follows the image...

Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.

<hr class="clear" />

```{% raw %}
{% include image.html url="assets/img/no_image.jpg"
   description="float left" class="left" %}
{% endraw %}```
{% include image.html url="assets/img/no_image.jpg" description="float left" class="left" %}

And sample text follows the image...

Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.

<hr class="clear" />

### Image Floating (old method, not recommended)

This is the CSS trick to align images in markdown document.

1. If you add image with alternative text start by "center", the image will be centered.
1. If you add image with alternative text start by "left", the image will be floated and aligned to left.
1. If you add image with alternative text start by "right", the image will be floated and aligned to right.
1. To clear floating, `<hr class="clear" />` can be used.

Examples:

```markdown
![center](assets/img/no_image.jpg) and sample text follows the image
```
![center](assets/img/no_image.jpg)
*example of caption*

and sample text follows the image.

<hr class="clear">

```markdown
![left](assets/img/no_image.jpg)
```
![left](assets/img/no_image.jpg) and sample text follows the image.

Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.


```markdown
![right](assets/img/no_image.jpg)
```
![right](assets/img/no_image.jpg)

and sample text follows the image.

Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
Text to check behavior or floated text.
