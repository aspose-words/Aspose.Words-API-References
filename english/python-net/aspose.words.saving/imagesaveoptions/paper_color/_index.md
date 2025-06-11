---
title: ImageSaveOptions.paper_color property
linktitle: paper_color property
articleTitle: paper_color property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.paper_color property. Gets or sets the background (paper) color for the generated images"
type: docs
weight: 110
url: /python-net/aspose.words.saving/imagesaveoptions/paper_color/
---

## ImageSaveOptions.paper_color property

Gets or sets the background (paper) color for the generated images.
The default value is aspose.pydrawing.Color.white.




```python
@property
def paper_color(self) -> aspose.pydrawing.Color:
    ...

@paper_color.setter
def paper_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

When rendering pages of a document that specifies its own background color,
then the document background color will override the color specified by this property.




### Examples

Renders a page of a Word document into an image with transparent or colored background.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Times New Roman'
builder.font.size = 24
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
# to modify the way in which that method renders the document into an image.
img_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Set the "PaperColor" property to a transparent color to apply a transparent
# background to the document while rendering it to an image.
img_options.paper_color = aspose.pydrawing.Color.transparent
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.PaperColor.Transparent.png', save_options=img_options)
# Set the "PaperColor" property to an opaque color to apply that color
# as the background of the document as we render it to an image.
img_options.paper_color = aspose.pydrawing.Color.light_coral
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.PaperColor.LightCoral.png', save_options=img_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

