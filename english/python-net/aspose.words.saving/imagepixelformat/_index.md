﻿---
title: ImagePixelFormat enumeration
linktitle: ImagePixelFormat enumeration
articleTitle: ImagePixelFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImagePixelFormat enumeration. Specifies the pixel format for the generated images of document pages."
type: docs
weight: 380
url: /python-net/aspose.words.saving/imagepixelformat/
---

## ImagePixelFormat enumeration

Specifies the pixel format for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| FORMAT_16BPP_RGB_555 | 16 bits per pixel, RGB. |
| FORMAT_16BPP_RGB_565 | 16 bits per pixel, RGB. |
| FORMAT_16BPP_ARGB_1555 | 16 bits per pixel, ARGB. |
| FORMAT_24BPP_RGB | 24 bits per pixel, RGB. |
| FORMAT_32BPP_RGB | 32 bits per pixel, RGB. |
| FORMAT_32BPP_ARGB | 32 bits per pixel, ARGB. |
| FORMAT_32BPP_P_ARGB | 32 bits per pixel, ARGB, premultiplied alpha. |
| FORMAT_48BPP_RGB | 48 bits per pixel, RGB. |
| FORMAT_64BPP_ARGB | 64 bits per pixel, ARGB. |
| FORMAT_64BPP_P_ARGB | 64 bits per pixel, ARGB, premultiplied alpha. |
| FORMAT_1BPP_INDEXED | 1 bit per pixel, Indexed. |

### Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# When we save the document as an image, we can pass a SaveOptions object to
# select a pixel format for the image that the saving operation will generate.
# Various bit per pixel rates will affect the quality and file size of the generated image.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.pixel_format = image_pixel_format
# We can clone ImageSaveOptions instances.
self.assertNotEqual(image_save_options, image_save_options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.PixelFormat.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

