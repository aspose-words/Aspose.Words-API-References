---
title: WrapSide enumeration
linktitle: WrapSide enumeration
articleTitle: WrapSide enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.WrapSide enumeration. Specifies what side(s) of the shape or picture the text wraps around."
type: docs
weight: 520
url: /python-net/aspose.words.drawing/wrapside/
---

## WrapSide enumeration

Specifies what side(s) of the shape or picture the text wraps around.


### Members

| Name | Description |
| --- | --- |
| BOTH | The document text wraps on both sides of the shape. |
| LEFT | The document text wraps on the left side of the shape only. There is a text free area on the right of the shape. |
| RIGHT | The document text wraps on the right side of the shape only. There is a text free area on the left side of the shape. |
| LARGEST | The document text wraps on the side of the shape that is farthest from the page margin, leaving text free area on the other side of the shape. |
| DEFAULT | Default value is [WrapSide.BOTH](./#BOTH). |

### Examples

Shows how to replace all textbox shapes with image shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Textboxes in drawing canvas.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(3, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(1, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
for shape in shapes:
    if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX:
        replacement_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
        replacement_shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
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
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(0, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(4, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ReplaceTextboxesWithImages.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.wrap_side](../shapebase/wrap_side/)

