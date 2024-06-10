---
title: ImageSaveOptions.pixel_format property
linktitle: pixel_format property
articleTitle: pixel_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.pixel_format property. Gets or sets the pixel format for the generated images."
type: docs
weight: 110
url: /python-net/aspose.words.saving/imagesaveoptions/pixel_format/
---

## ImageSaveOptions.pixel_format property

Gets or sets the pixel format for the generated images.


```python
@property
def pixel_format(self) -> aspose.words.saving.ImagePixelFormat:
    ...

@pixel_format.setter
def pixel_format(self, value: aspose.words.saving.ImagePixelFormat):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT_32BPP_ARGB](../../imagepixelformat/#FORMAT_32BPP_ARGB).

Pixel format of the output image may differ from the set value
because of work of GDI+.




### Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
self.assertLess(20000, os.path.getsize(IMAGE_DIR + 'Logo.jpg'))
# When we save the document as an image, we can pass a SaveOptions object to
# select a pixel format for the image that the saving operation will generate.
# Various bit per pixel rates will affect the quality and file size of the generated image.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.pixel_format = image_pixel_format
# We can clone ImageSaveOptions instances.
self.assertNotEqual(image_save_options, image_save_options.clone())
doc.save(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png', image_save_options)
if image_pixel_format == aw.saving.ImagePixelFormat.FORMAT_1BPP_INDEXED:
    self.assertGreater(10000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png'))
elif image_pixel_format == aw.saving.ImagePixelFormat.FORMAT_16BPP_RGB_555:
    self.assertLess(125000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png'))
elif image_pixel_format == aw.saving.ImagePixelFormat.FORMAT_24BPP_RGB:
    self.assertLess(70000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png'))
elif image_pixel_format == aw.saving.ImagePixelFormat.FORMAT_32BPP_RGB:
    self.assertLess(125000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png'))
elif image_pixel_format == aw.saving.ImagePixelFormat.FORMAT_48BPP_RGB:
    self.assertLess(125000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.pixel_format.png'))
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

