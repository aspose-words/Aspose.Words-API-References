---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 120
url: /python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.

The default value is 1.0. The value must be greater than 0.


### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.paragraph_format.style = doc.styles.get_by_name("Heading 1")
builder.writeln("Hello world!")
builder.insert_image(IMAGE_DIR + "Logo.jpg")

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

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.edit_image.png", options)
```

Shows how to render an Office Math object into an image file in the local file system.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()

# Create an "ImageSaveOptions" object to pass to the node renderer's "save" method to modify
# how it renders the OfficeMath node into an image.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)

# Set the "scale" property to 5 to render the object to five times its original size.
save_options.scale = 5

math.get_math_renderer().save(ARTIFACTS_DIR + "Shape.render_office_math.png", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

