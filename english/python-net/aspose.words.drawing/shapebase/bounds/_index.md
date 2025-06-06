﻿---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /python-net/aspose.words.drawing/shapebase/bounds/
---

## ShapeBase.bounds property

Gets or sets the location and size of the containing block of the shape.


```python
@property
def bounds(self) -> aspose.pydrawing.RectangleF:
    ...

@bounds.setter
def bounds(self, value: aspose.pydrawing.RectangleF):
    ...

```

### Remarks

Ignores aspect ratio lock upon setting.


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# Create a group shape. A group shape can display a collection of child shape nodes.
# In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
# select all the other child shapes within this group and allow us to scale and move all the shapes at once.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Set the group's internal coordinate plane size to 500 x 500pt.
# The top left corner of the group will have an x and y coordinate of (0, 0),
# and the bottom right corner will have an x and y coordinate of (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Set the coordinates of the top left corner of the group to (-250, -250).
# The group's center will now have an x and y coordinate value of (0, 0),
# and the bottom right corner will be at (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Create a rectangle that will display the boundary of this group shape and add it to the group.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Once a shape is a part of a group shape, we can access it as a child node and then modify it.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Create a small red star and insert it into the group.
# Line up the shape with the group's coordinate origin, which we have moved to the center.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
# Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
# and then the shape with the image will overlap the light blue rectangle, using it as a frame.
# We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
child3 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child3.width = 250
child3.height = 250
child3.left = -250
child3.top = -250
child3.fill_color = aspose.pydrawing.Color.light_blue
group.append_child(child3)
child4 = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
child4.width = 200
child4.height = 200
child4.left = -225
child4.top = -225
group.append_child(child4)
group.get_child(aw.NodeType.SHAPE, 3, True).as_shape().image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
# touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
# the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
child5 = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
child5.width = 200
child5.height = 50
child5.left = group.coord_size.width + group.coord_origin.x - 200
child5.top = group.coord_size.height + group.coord_origin.y
group.append_child(child5)
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(group)
builder.move_to(group.get_child(aw.NodeType.SHAPE, 4, True).as_shape().append_child(aw.Paragraph(doc)))
builder.write('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GroupShape.docx')
```

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Even though the line itself takes up little space on the document page,
# it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Create a group shape, and then set the size of its containing block using the "Bounds" property.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
# and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
# Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
# translates to 1pt in the document body's coordinate plane.
# Every shape that we insert will also shrink in size by a factor of 4.
# The change in the shape's "BoundsInPoints" property will reflect this.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Insert a shape and place it outside of the bounds of the group shape's containing block.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# The group shape's footprint in the document body has increased, but the containing block remains the same.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

