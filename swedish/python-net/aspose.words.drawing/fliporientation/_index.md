---
title: FlipOrientation enumeration
linktitle: FlipOrientation enumeration
articleTitle: FlipOrientation enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.FlipOrientation enumeration. Possible values for the orientation of a shape."
type: docs
weight: 100
url: /sv/python-net/aspose.words.drawing/fliporientation/
---

## FlipOrientation enumeration

Possible values for the orientation of a shape.


### Members

| Name | Description |
| --- | --- |
| NONE | Coordinates are not flipped. |
| HORIZONTAL | Flip along the y-axis, reversing the x-coordinates. |
| VERTICAL | Flip along the x-axis, reversing the y-coordinates. |
| BOTH | Flip along both the y- and x-axis. |

### Examples

Shows how to flip a shape on an axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga en bildform och låt dess orientering vara i standardläget.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
self.assertEqual(aw.drawing.FlipOrientation.NONE, shape.flip_orientation)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=250, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Sätt egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den andra formen på y-axeln,
# så att den blir en horisontell spegelbild av den första formen.
shape.flip_orientation = aw.drawing.FlipOrientation.HORIZONTAL
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=250, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den tredje formen på x-axeln,
# gör den till en vertikal spegelbild av den första formen.
shape.flip_orientation = aw.drawing.FlipOrientation.VERTICAL
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=250, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=250, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den fjärde formen på både x- och y-axlarna,
# gör den till en horisontell och vertikal spegelbild av den första formen.
shape.flip_orientation = aw.drawing.FlipOrientation.BOTH
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FlipShapeOrientation.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.flip_orientation](../shapebase/flip_orientation/)

