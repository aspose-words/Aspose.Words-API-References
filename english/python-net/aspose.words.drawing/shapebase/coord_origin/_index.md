---
title: ShapeBase.coord_origin property
linktitle: coord_origin property
articleTitle: coord_origin property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_origin property. The coordinates at the top-left corner of the containing block of this shape."
type: docs
weight: 110
url: /python-net/aspose.words.drawing/shapebase/coord_origin/
---

## ShapeBase.coord_origin property

The coordinates at the top-left corner of the containing block of this shape.


```python
@property
def coord_origin(self) -> aspose.pydrawing.Point:
    ...

@coord_origin.setter
def coord_origin(self, value: aspose.pydrawing.Point):
    ...

```

### Remarks

The default value is (0,0).




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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Insert a group shape, and place it 100 points below and to the right of
# the document's x and Y coordinate origin point.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
# lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# By default, a shape's internal coordinate plane has the top left corner at (0, 0),
# and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
# in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
# to a movement of 2pts on the group shape's coordinate plane.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Move the group shape's x and y axis origin from the top left corner to the center.
# This will offset the group's internal coordinates relative to the document's coordinates even further.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Changing the scale of the coordinate plane will also affect relative locations.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# If we wish to add a shape to this group while defining its location based on a location in the document,
# we will need to first confirm a location in the group shape that will match the document's location.
self.assertEqual(aspose.pydrawing.PointF(700, 700), group.local_to_parent(aspose.pydrawing.PointF(350, 350)))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LocalToParent.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

