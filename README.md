nginx image_filter
-----

This is basically the same [image_filter](ngx_http_image_filter_module) module, but with ability to place cropped images.

## Configuration

This module has additional configuration option:

```
image_filter_offset {left,center,right} {top,center,bottom};
```

## Examples

### Horizontal images

* Original image

![Original horizontal image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/horizontal-original.png "Original horizontal image")

* Crop and align to top: `image_filter_offset center top;`

![Aligned to top horizontal image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/horizontal-top.png "Aligned to top horizontal image")

* Crop and align to center (original behavior): `image_filter_offset center center;`

![Aligned to center horizontal image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/horizontal-center.png "Aligned to center horizontal image")

* Crop and align to bottom: `image_filter_offset center bottom;`

![Aligned to bottom horizontal image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/horizontal-bottom.png "Aligned to bottom horizontal image")

### Vertical images

* Original image

![Original vertical image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/vertical-original.png "Original vertical image")

* Crop and align to left: `image_filter_offset left center;`

![Aligned to left vertical image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/vertical-left.png "Aligned to left vertical image")

* Crop and align to center (original behavior): `image_filter_offset center center;`

![Aligned to center vertical image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/vertical-center.png "Aligned to center vertical image")

* Crop and align to right: `image_filter_offset right center;`

![Aligned to right vertical image](https://github.com/bobrik/nginx_image_filter/raw/master/examples/vertical-right.png "Aligned to right vertical image")

## Authors

* [Nginx authors](http://nginx.org/)
* [Ian Babrou](https://github.com/bobrik)
