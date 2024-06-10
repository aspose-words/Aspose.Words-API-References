---
title: ShapeBase.wrap_side property
linktitle: wrap_side property
articleTitle: wrap_side property
second_title: Aspose.Words for Python
description: "ShapeBase.wrap_side property. Specifies how the text is wrapped around the shape."
type: docs
weight: 620
url: /python-net/aspose.words.drawing/shapebase/wrap_side/
---

## ShapeBase.wrap_side property

Specifies how the text is wrapped around the shape.


```python
@property
def wrap_side(self) -> aspose.words.drawing.WrapSide:
    ...

@wrap_side.setter
def wrap_side(self, value: aspose.words.drawing.WrapSide):
    ...

```

### Remarks

The default value is [WrapSide.BOTH](../../wrapside/#BOTH).

Has effect only for top level shapes.




### Examples

Shows how to replace all textbox shapes with image shapes.

```python
doc = aw.Document(MY_DIR + 'Textboxes in drawing canvas.docx')
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]
self.assertEqual(3, len([shape for shape in shapes if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX]))
self.assertEqual(1, len([shape for shape in shapes if shape.shape_type == aw.drawing.ShapeType.IMAGE]))
for shape in shapes:
    if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX:
        replacement_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
        replacement_shape.image_data.set_image(IMAGE_DIR + 'Logo.jpg')
        replacement_shape.left = shape.left
        replacement_shape.top = shape.top
        replacement_shape.width = shape.width
        replacement_shape.height = shape.height
        replacement_shape.relative_horizontal_position = shape.relative_horizontal_position
        replacement_shape.relative_vertical_position = shape.relative_vertical_position
        replacement_shape.horizontal_alignment = shape.horizontal_alignment
        replacement_shape.vertical_alignment = shape.vertical_alignment
        replacement_shape.wrap_type = shape.wrap_type
        replacement_shape.wrap_side = shape.wrap_side
        shape.parent_node.insert_after(replacement_shape, shape)
        shape.remove()
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]
self.assertEqual(0, len([shape for shape in shapes if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX]))
self.assertEqual(4, len([shape for shape in shapes if shape.shape_type == aw.drawing.ShapeType.IMAGE]))
doc.save(ARTIFACTS_DIR + 'Shape.replace_textboxes_with_images.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

