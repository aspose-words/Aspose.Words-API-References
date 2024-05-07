---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 670
url: /python-net/aspose.words.drawing/shapebase/local_to_parent/
---

## local_to_parent(value) {#pointf}

Converts a value from the local coordinate space into the coordinate space of the parent shape.


```python
def local_to_parent(self, value: aspose.pydrawing.PointF):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | aspose.pydrawing.PointF |  |

### Examples

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()

# Insert a group shape, and place it 100 points below and to the right of
# the document's x and Y coordinate origin point.
group = aw.drawing.GroupShape(doc)
group.bounds = drawing.RectangleF(100, 100, 500, 500)

# Use the "local_to_parent" method to determine that (0, 0) on the group's internal x and y coordinates
# lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
self.assertEqual(drawing.PointF(100, 100), group.local_to_parent(drawing.PointF(0, 0)))

# By default, a shape's internal coordinate plane has the top left corner at (0, 0),
# and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
# in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
# to a movement of 2pts on the group shape's coordinate plane.
self.assertEqual(drawing.PointF(150, 150), group.local_to_parent(drawing.PointF(100, 100)))
self.assertEqual(drawing.PointF(200, 200), group.local_to_parent(drawing.PointF(200, 200)))
self.assertEqual(drawing.PointF(250, 250), group.local_to_parent(drawing.PointF(300, 300)))

# Move the group shape's x and y axis origin from the top left corner to the center.
# This will offset the group's internal coordinates relative to the document's coordinates even further.
group.coord_origin = drawing.Point(-250, -250)

self.assertEqual(drawing.PointF(375, 375), group.local_to_parent(drawing.PointF(300, 300)))

# Changing the scale of the coordinate plane will also affect relative locations.
group.coord_size = drawing.Size(500, 500)

self.assertEqual(drawing.PointF(650, 650), group.local_to_parent(drawing.PointF(300, 300)))

# If we wish to add a shape to this group while defining its location based on a location in the document,
# we will need to first confirm a location in the group shape that will match the document's location.
self.assertEqual(drawing.PointF(700, 700), group.local_to_parent(drawing.PointF(350, 350)))

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700

group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)

doc.save(ARTIFACTS_DIR + "Shape.local_to_parent.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

