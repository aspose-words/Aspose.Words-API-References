﻿---
title: ImageSaveOptions.image_brightness property
linktitle: image_brightness property
articleTitle: image_brightness property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_brightness property. Gets or sets the brightness for the generated images."
type: docs
weight: 30
url: /python-net/aspose.words.saving/imagesaveoptions/image_brightness/
---

## ImageSaveOptions.image_brightness property

Gets or sets the brightness for the generated images.


```python
@property
def image_brightness(self) -> float:
    ...

@image_brightness.setter
def image_brightness(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.




### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# When we save the document as an image, we can pass a SaveOptions object to
# edit the image while the saving operation renders it.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# We can adjust these properties to change the image's brightness and contrast.
# Both are on a 0-1 scale and are at 0.5 by default.
options.image_brightness = 0.3
options.image_contrast = 0.7
# We can adjust horizontal and vertical resolution with these properties.
# This will affect the dimensions of the image.
# The default value for these properties is 96.0, for a resolution of 96dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# We can scale the image using this property. The default value is 1.0, for scaling of 100%.
# We can use this property to negate any changes in image dimensions that changing the resolution would cause.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

