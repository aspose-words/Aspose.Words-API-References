---
title: ShapeBase.left property
linktitle: left property
articleTitle: left property
second_title: Aspose.Words for Python
description: "ShapeBase.left property. Gets or sets the position of the left edge of the containing block of the shape."
type: docs
weight: 380
url: /python-net/aspose.words.drawing/shapebase/left/
---

## ShapeBase.left property

Gets or sets the position of the left edge of the containing block of the shape.


```python
@property
def left(self) -> float:
    ...

@left.setter
def left(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.wrap_type = aw.drawing.WrapType.NONE

# Configure the shape's "relative_horizontal_position" property to treat the value of the "left" property
# as the shape's horizontal distance, in points, from the left side of the page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE

# Set the shape's horizontal distance from the left side of the page to 100.
shape.left = 100

# Use the "relative_vertical_position" property in a similar way to position the shape 80pt below the top of the page.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80

# Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.height = 125

self.assertEqual(125.0, shape.width)

# The "bottom" and "right" properties contain the bottom and right edges of the image.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)

doc.save(ARTIFACTS_DIR + "Image.create_floating_position_size.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

