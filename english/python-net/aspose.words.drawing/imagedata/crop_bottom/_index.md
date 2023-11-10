---
title: ImageData.crop_bottom property
linktitle: crop_bottom property
articleTitle: crop_bottom property
second_title: Aspose.Words for Python
description: "ImageData.crop_bottom property. Defines the fraction of picture removal from the bottom side."
type: docs
weight: 60
url: /python-net/aspose.words.drawing/imagedata/crop_bottom/
---

## ImageData.crop_bottom property

Defines the fraction of picture removal from the bottom side.


```python
@property
def crop_bottom(self) -> float:
    ...

@crop_bottom.setter
def crop_bottom(self, value: float):
    ...

```

### Remarks

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note 
that a value of 1 will display no picture at all. Negative values will result in 
the picture being squeezed inward from the edge being cropped (the empty space 
between the picture and the cropped edge will be filled by the fill color of the 
shape). Positive values less than 1 will result in the remaining picture being 
stretched to fit the shape.

The default value is 0.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(MY_DIR + "Images.docx")
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()

dst_doc = aw.Document()

# Import a shape from the source document and append it to the first paragraph.
imported_shape = dst_doc.import_node(source_shape, True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)

# The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
image_data = imported_shape.image_data
image_data.title = "Imported Image"

self.assertTrue(image_data.has_image)

# If an image has no borders, its "image_data" object will define the border color as empty.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(drawing.Color.empty(), image_data.borders[0].color)

# This image does not link to another shape or image file in the local file system.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)

# The "brightness" and "contrast" properties define image brightness and contrast
# on a 0-1 scale, with the default value at 0.5.
image_data.brightness = 0.8
image_data.contrast = 1.0

# The above brightness and contrast values have created an image with a lot of white.
# We can select a color with the ChromaKey property to replace with transparency, such as white.
image_data.chroma_key = drawing.Color.white

# Import the source shape again and set the image to monochrome.
imported_shape = dst_doc.import_node(source_shape, True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)

imported_shape.image_data.gray_scale = True

# Import the source shape again to create a third image and set it to "bi_level".
# "bi_level" sets every pixel to either black or white, whichever is closer to the original color.
imported_shape = dst_doc.import_node(source_shape, True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)

imported_shape.image_data.bi_level = True

# Cropping is determined on a 0-1 scale. Cropping a side by 0.3
# will crop 30% of the image out at the cropped side.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3

dst_doc.save(ARTIFACTS_DIR + "Drawing.image_data.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

