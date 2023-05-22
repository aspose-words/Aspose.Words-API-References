---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /python-net/aspose.words.drawing/shapebase/bounds_in_points/
---

## ShapeBase.bounds_in_points property

Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.


### Examples

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.LINE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 50,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 50, 100, 100, aw.drawing.WrapType.NONE)
shape.stroke_color = drawing.Color.orange

# Even though the line itself takes up little space on the document page,
# it occupies a rectangular containing block, the size of which we can determine using the "bounds" properties.
self.assertEqual(drawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(drawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)

# Create a group shape, and then set the size of its containing block using the "Bounds" property.
group = aw.drawing.GroupShape(doc)
group.bounds = drawing.RectangleF(0, 100, 250, 250)

self.assertEqual(drawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)

# Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700

self.assertEqual(drawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)

group.append_child(shape)

# The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
# and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
# Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
# translates to 1pt in the document body's coordinate plane.
# Every shape that we insert will also shrink in size by a factor of 4.
# The change in the shape's "bounds_in_points" property will reflect this.
self.assertEqual(drawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)

doc.first_section.body.first_paragraph.append_child(group)

# Insert a shape and place it outside of the bounds of the group shape's containing block.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000

group.append_child(shape)

# The group shape's footprint in the document body has increased, but the containing block remains the same.
self.assertEqual(drawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(drawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)

doc.save(ARTIFACTS_DIR + "Shape.bounds.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

