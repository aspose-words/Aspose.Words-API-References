---
title: ImageSaveOptions.image_contrast property
linktitle: image_contrast property
articleTitle: image_contrast property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_contrast property. Gets or sets the contrast for the generated images."
type: docs
weight: 50
url: /python-net/aspose.words.saving/imagesaveoptions/image_contrast/
---

## ImageSaveOptions.image_contrast property

Gets or sets the contrast for the generated images.


```python
@property
def image_contrast(self) -> float:
    ...

@image_contrast.setter
def image_contrast(self, value: float):
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
options.image_brightness = 0.3
options.image_contrast = 0.7
options.horizontal_resolution = 72
options.vertical_resolution = 72
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

