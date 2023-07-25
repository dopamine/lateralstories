---
title: "Photo post example"
layout: post
tags:
  - image
  - Post Formats
---
{% include toc.html %}

## How to insert images

1. Create new folder matching post file name on Dropbox
1. Copy post image files into that folder
1. Reference images as `{% raw %}![alt text]({{ site.imgsrc }}/post-name/image.jpg){% endraw %}`

### Example images hosted on R2 bucket

![WHW Doune bothy]({{ site.imgsrc }}/posts/1970-01-01-test/whw-doune-bothy.JPG)
![Snow day street]({{ site.imgsrc }}/posts/1970-01-01-test/utca.jpeg)
![Snow sheep Pentlands]({{ site.imgsrc }}/posts/1970-01-01-test/pentlands-sheep-braefoot-bay.jpeg)
![Mallorca serpentine]({{ site.imgsrc }}/posts/1970-01-01-test/mallorca-serpentine.jpg)


## Styling and aligning images

By default, images are 100% width of the post body.

It is possible to override this with `.noresize`, so images appear at their original size, but still bound by maximum width of 100%.

Additionally, there are two `.punch-*` classes and `.extra-wide` available to punch images out left, or right, or in both directions, for added layout interest.

To adjust the styling/alignment of post images, use this notation:
```
{% raw %}![alt text]({{ site.imgsrc }}/post-name/image.jpg){:.class }{% endraw %}
```

### Examples in use

`default styling - horizontal`  
![alt text](http://placekitten.com/800/200)

`default styling - vertical`  
![alt text](http://placekitten.com/400/600)

`small image`  
![alt text](http://placekitten.com/400/600){:.noresize}

`default`  
![alt text](http://placekitten.com/800/200)

`punch left`  
![alt text](http://placekitten.com/800/200){:.punch-left}

`punch right`  
![alt text](http://placekitten.com/800/200){:.punch-right}

`extra wide`  
![alt text](http://placekitten.com/1200/200){:.extra-wide}