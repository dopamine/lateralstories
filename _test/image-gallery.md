---
title: "Image gallery example"
layout: post
tags:
  - gallery
  - Post Formats
  - tiled
gallery:
  - url: http://xiple.co.uk
    image_path: http://placekitten.com/200/200
    alt: "placeholder image"
  - url: http://xiple.co.uk
    image_path: http://placekitten.com/200/200
    alt: "placeholder image"
  - url: http://xiple.co.uk
    image_path: http://placekitten.com/200/200
    alt: "placeholder image"
  - url: http://xiple.co.uk
    image_path: http://placekitten.com/200/200
    alt: "placeholder image"
gallery2:
  - url: https://flic.kr/p/8a6Ven
    image_path: https://farm2.staticflickr.com/1272/4697500467_8294dac099_q.jpg
    alt: "Black and grays with a hint of green"
  - url: https://flic.kr/p/8a738X
    image_path: https://farm5.staticflickr.com/4029/4697523701_249e93ba23_q.jpg
    alt: "Made for open text placement"
  - url: https://flic.kr/p/8a6VXP
    image_path: https://farm5.staticflickr.com/4046/4697502929_72c612c636_q.jpg
    alt: "Fog in the trees"
gallery3:
  - image_path: http://placekitten.com/200/200
    alt: "placeholder image"
  - image_path: http://placekitten.com/200/200
    alt: "placeholder image"
---

These are gallery tests for image wrapped in `<figure>` elements.

To place a gallery add the necessary YAML Front Matter:

```yaml
gallery:
  - url: unsplash-gallery-image-1.jpg
    image_path: unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: unsplash-gallery-image-2.jpg
    image_path: unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: unsplash-gallery-image-3.jpg
    image_path: unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
  - url: unsplash-gallery-image-4.jpg
    image_path: unsplash-gallery-image-4-th.jpg
    alt: "placeholder image 4"
```

And then drop-in the gallery include --- gallery `caption` is optional.

```liquid
{% raw %}{% include gallery.html caption="This is a sample gallery with **Markdown support**." %}{% endraw %}
```

{% include gallery.html caption="This is a sample gallery with **Markdown support**." %}

This is some text after the gallery just to make sure that everything aligns properly.

Here comes another gallery, this time set the `id` to match 2nd gallery hash in YAML Front Matter.

```yaml
gallery2:
  - url: https://flic.kr/p/8a6Ven
    image_path: https://farm2.staticflickr.com/1272/4697500467_8294dac099_q.jpg
    alt: "Black and grays with a hint of green"
  - url: https://flic.kr/p/8a738X
    image_path: https://farm5.staticflickr.com/4029/4697523701_249e93ba23_q.jpg
    alt: "Made for open text placement"
  - url: https://flic.kr/p/8a6VXP
    image_path: https://farm5.staticflickr.com/4046/4697502929_72c612c636_q.jpg
    alt: "Fog in the trees"
```

And place it like so: 

```liquid
{% raw %}{% include gallery.html id="gallery2" caption="This is a second gallery example with images hosted externally." %}{% endraw %}
```

{% include gallery.html id="gallery2" caption="This is a second gallery example with images hosted externally." %}

And for giggles one more gallery just to make sure this works. To fill page content container add `class="full"`.

{% include gallery.html id="gallery3" class="full" caption="This is a third gallery example with two images and fills the entire content container." %}