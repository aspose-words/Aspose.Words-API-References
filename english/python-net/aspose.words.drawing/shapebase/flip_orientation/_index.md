---
title: flip_orientation property
second_title: Aspose.Words for Python via .NET API Reference
description: "Switches the orientation of a shape."
type: docs
weight: 180
url: /python-net/aspose.words.drawing/shapebase/flip_orientation/
---

## ShapeBase.flip_orientation property

Switches the orientation of a shape.

The default value is [FlipOrientation.NONE](../../fliporientation/#NONE).




### Examples

Shows how to flip a shape on an axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert an image shape and leave its orientation in its default state.
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 100, 100, 100, aw.drawing.WrapType.NONE)
shape.image_data.set_image(IMAGE_DIR + "Logo.jpg")

self.assertEqual(aw.drawing.FlipOrientation.NONE, shape.flip_orientation)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 250,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 100, 100, 100, aw.drawing.WrapType.NONE)
shape.image_data.set_image(IMAGE_DIR + "Logo.jpg")

# Set the "flip_orientation" property to "FlipOrientation.HORIZONTAL" to flip the second shape on the y-axis,
# making it into a horizontal mirror image of the first shape.
shape.flip_orientation = aw.drawing.FlipOrientation.HORIZONTAL

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 250, 100, 100, aw.drawing.WrapType.NONE)
shape.image_data.set_image(IMAGE_DIR + "Logo.jpg")

# Set the "flip_orientation" property to "FlipOrientation.VERTICAL" to flip the third shape on the x-axis,
# making it into a vertical mirror image of the first shape.
shape.flip_orientation = aw.drawing.FlipOrientation.VERTICAL

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 250,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 250, 100, 100, aw.drawing.WrapType.NONE)
shape.image_data.set_image(IMAGE_DIR + "Logo.jpg")

# Set the "flip_orientation" property to "FlipOrientation.BOTH" to flip the fourth shape on both the x and y axes,
# making it into a horizontal and vertical mirror image of the first shape.
shape.flip_orientation = aw.drawing.FlipOrientation.BOTH

doc.save(ARTIFACTS_DIR + "Shape.flip_shape_orientation.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

