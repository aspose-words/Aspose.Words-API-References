---
title: ImageSaveOptions.image_color_mode property
linktitle: image_color_mode property
articleTitle: image_color_mode property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_color_mode property. Gets or sets the color mode for the generated images."
type: docs
weight: 40
url: /python-net/aspose.words.saving/imagesaveoptions/image_color_mode/
---

## ImageSaveOptions.image_color_mode property

Gets or sets the color mode for the generated images.


```python
@property
def image_color_mode(self) -> aspose.words.saving.ImageColorMode:
    ...

@image_color_mode.setter
def image_color_mode(self, value: aspose.words.saving.ImageColorMode):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../imagecolormode/#NONE).




### Examples

Shows how to set a color mode when rendering documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
self.assertLess(20000, os.path.getsize(IMAGE_DIR + 'Logo.jpg'))
# When we save the document as an image, we can pass a SaveOptions object to
# select a color mode for the image that the saving operation will generate.
# If we set the "image_color_mode" property to "ImageColorMode.BLACK_AND_WHITE",
# the saving operation will apply grayscale color reduction while rendering the document.
# If we set the "image_color_mode" property to "ImageColorMode.GRAYSCALE",
# the saving operation will render the document into a monochrome image.
# If we set the "image_color_mode" property to "NONE", the saving operation will apply the default method
# and preserve all the document's colors in the output image.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(ARTIFACTS_DIR + 'ImageSaveOptions.color_mode.png', image_save_options)
if image_color_mode == aw.saving.ImageColorMode.NONE:
    self.assertLess(120000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.color_mode.png'))
elif image_color_mode == aw.saving.ImageColorMode.GRAYSCALE:
    self.assertLess(80000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.color_mode.png'))
elif image_color_mode == aw.saving.ImageColorMode.BLACK_AND_WHITE:
    self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.color_mode.png'))
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

