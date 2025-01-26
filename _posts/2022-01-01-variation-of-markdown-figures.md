---
layout: post
title: Special markdown syntax for image layouts
image: https://hbb.afl.rakuten.co.jp/hgb/1ee40173.5e0d8bb1.1ee40174.f69272c5/?me_id=1205150&item_id=10004413&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fchamp%2Fcabinet%2Fkarate%2Fimg60748112.jpg%3F_ex%3D400x400&s=400x400&t=pict
description: This article shows example of special image keywrods supported by this theme.
tags: feature doc
doc_index: 100
---
In this theme, alternate string for a image affects to image layout.

## Normal Markdown Syntax to Place an Image

Normally, images are centered in the page.
```
![](https://hbb.afl.rakuten.co.jp/hgb/1ee40173.5e0d8bb1.1ee40174.f69272c5/?me_id=1205150&item_id=10004413&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fchamp%2Fcabinet%2Fkarate%2Fimg60748112.jpg%3F_ex%3D400x400&s=400x400&t=pict)
```

![](https://hbb.afl.rakuten.co.jp/hgb/1ee40173.5e0d8bb1.1ee40174.f69272c5/?me_id=1205150&item_id=10004413&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fchamp%2Fcabinet%2Fkarate%2Fimg60748112.jpg%3F_ex%3D400x400&s=400x400&t=pict)

## Special Syntax for Alternate String

### Floating image

Float image to right: when the alternative text for the image includes `right`, the image is treated as floating image.
```
![right](https://1.bp.blogspot.com/-36JFMZJkRzQ/YGb7rmCVUII/AAAAAAAAjls/PJqguHshxvEO40z9sIOTRk0ctQVN1B1pQCLcBGAsYHQ/s400/judo_boy_w_mask.jpg)
```

![right](https://1.bp.blogspot.com/-36JFMZJkRzQ/YGb7rmCVUII/AAAAAAAAjls/PJqguHshxvEO40z9sIOTRk0ctQVN1B1pQCLcBGAsYHQ/s400/judo_boy_w_mask.jpg)

Clear: and to clear the floating, `hr` element with `clear` class can be used.
```
<hr class="clear">
```

<hr class="clear">

Similar as `right`, `left` in alternative makes image floated to left.
```
![left](https://1.bp.blogspot.com/-36JFMZJkRzQ/YGb7rmCVUII/AAAAAAAAjls/PJqguHshxvEO40z9sIOTRk0ctQVN1B1pQCLcBGAsYHQ/s400/judo_boy_w_mask.jpg)
```

![left](https://1.bp.blogspot.com/-36JFMZJkRzQ/YGb7rmCVUII/AAAAAAAAjls/PJqguHshxvEO40z9sIOTRk0ctQVN1B1pQCLcBGAsYHQ/s400/judo_boy_w_mask.jpg)

These floating images are enabled by regular expression `^right` and `^left`, following markdown also treated as floating image:
```
![left:addtional notes](https://example.com/example.jpg)
```
