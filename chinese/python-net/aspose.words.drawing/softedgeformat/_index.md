---
title: SoftEdgeFormat class
linktitle: SoftEdgeFormat class
articleTitle: SoftEdgeFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.SoftEdgeFormat class. Represents the soft edge formatting for an object."
type: docs
weight: 430
url: /zh/python-net/aspose.words.drawing/softedgeformat/
---

## SoftEdgeFormat class

Represents the soft edge formatting for an object.


### Remarks

Use the [ShapeBase.soft_edge](../shapebase/soft_edge/) property to access soft edge properties of an object.
You do not create instances of the [SoftEdgeFormat](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [radius](./radius/) | Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes [SoftEdgeFormat](./) from the parent object. |

### Examples

Shows how to work with soft edge formatting.

```python
builder = aw.DocumentBuilder()
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=200)
# 对形状应用柔和边缘。
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# 加载带有柔和边缘的矩形形状的文档。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
soft_edge_format = shape.soft_edge
# 检查柔和边缘半径。
self.assertEqual(30, soft_edge_format.radius)
# 从形状中移除柔和边缘。
soft_edge_format.remove()
# 检查已移除柔和边缘的半径。
self.assertEqual(0, soft_edge_format.radius)
```

### See Also

* module [aspose.words.drawing](../)

