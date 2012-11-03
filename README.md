nginx image_filter
-----

This is basically the same [image_filter](http://nginx.org/en/docs/http/ngx_http_image_filter_module.html) module, but with ability to place cropped images.

## Goals

Humans usually have faces at the top of their photos, but nginx always crop image to center. We needed to make it more flexible.

## Configuration

This module has additional configuration option:

```
image_filter_offset {left,center,right} {top,center,bottom};
```

## Examples

### Vertical images

* Original image

![Original vertical image](https://raw.github.com/bobrik/nginx_image_filter/master/example/vertical-original.jpg "Original vertical image")

* Crop and align to top: `image_filter_offset center top;`

![Aligned to top vertical image](https://raw.github.com/bobrik/nginx_image_filter/master/example/vertical-top.jpg "Aligned to top vertical image")

* Crop and align to center (original behavior): `image_filter_offset center center;`

![Aligned to center vertical image](https://raw.github.com/bobrik/nginx_image_filter/master/example/vertical-center.jpg "Aligned to center vertical image")

* Crop and align to bottom: `image_filter_offset center bottom;`

![Aligned to bottom vertical image](https://raw.github.com/bobrik/nginx_image_filter/master/example/vertical-bottom.jpg "Aligned to bottom vertical image")

### Horizontal images

* Original image

![Original horizontal image](https://raw.github.com/bobrik/nginx_image_filter/master/example/horizontal-original.jpg "Original horizontal image")

* Crop and align to left: `image_filter_offset left center;`

![Aligned to left horizontal image](https://raw.github.com/bobrik/nginx_image_filter/master/example/horizontal-left.jpg "Aligned to left horizontal image")

* Crop and align to center (original behavior): `image_filter_offset center center;`

![Aligned to center horizontal image](https://raw.github.com/bobrik/nginx_image_filter/master/example/horizontal-center.jpg "Aligned to center horizontal image")

* Crop and align to right: `image_filter_offset right center;`

![Aligned to right horizontal image](https://raw.github.com/bobrik/nginx_image_filter/master/example/horizontal-right.jpg "Aligned to right horizontal image")

## Authors

* [Nginx authors](http://nginx.org/)
* [Ian Babrou](https://github.com/bobrik)
