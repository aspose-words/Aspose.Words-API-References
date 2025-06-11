---
title: ImageSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "ImageSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 200
url: /python-net/aspose.words.saving/imagesaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```python
def clone(self):
    ...
```

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

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

