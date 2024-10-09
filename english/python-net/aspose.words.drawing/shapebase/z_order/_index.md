---
title: ShapeBase.z_order property
linktitle: z_order property
articleTitle: z_order property
second_title: Aspose.Words for Python
description: "ShapeBase.z_order property. Determines the display order of overlapping shapes."
type: docs
weight: 650
url: /python-net/aspose.words.drawing/shapebase/z_order/
---

## ShapeBase.z_order property

Determines the display order of overlapping shapes.


```python
@property
def z_order(self) -> int:
    ...

@z_order.setter
def z_order(self, value: int):
    ...

```

### Remarks

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed
as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main
text of the document.

The display order of child shapes in a group shape is determined by their order
inside the group shape.




### Examples

Shows how to manipulate the order of shapes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert three different colored rectangles that partially overlap each other.
# When we insert a shape that overlaps another shape, Aspose.Words places the newer shape on top of the old one.
# The light green rectangle will overlap the light blue rectangle and partially obscure it,
# and the light blue rectangle will obscure the orange rectangle.
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 100, aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 100, 200, 200, aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 150, aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 150, 200, 200, aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_blue
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 200, aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 200, 200, 200, aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_green
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]
# The "z_order" property of a shape determines its stacking priority among other overlapping shapes.
# If two overlapping shapes have different "z_order" values,
# Microsoft Word will place the shape with a higher value over the shape with the lower value.
# Set the "z_order" values of our shapes to place the first orange rectangle over the second light blue one
# and the second light blue rectangle over the third light green rectangle.
# This will reverse their original stacking order.
shapes[0].z_order = 3
shapes[1].z_order = 2
shapes[2].z_order = 1
doc.save(ARTIFACTS_DIR + 'Shape.z_order.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)
* property [ShapeBase.behind_text](../behind_text/)

