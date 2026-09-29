---
title: SoftEdgeFormat class
linktitle: SoftEdgeFormat class
articleTitle: SoftEdgeFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.SoftEdgeFormat class. Represents the soft edge formatting for an object."
type: docs
weight: 430
url: /sv/python-net/aspose.words.drawing/softedgeformat/
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
# Applicera mjuk kant på formen.
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# Läs in dokument med rektangelform med mjuk kant.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
soft_edge_format = shape.soft_edge
# Kontrollera radien för mjuk kant.
self.assertEqual(30, soft_edge_format.radius)
# Ta bort mjuk kant från formen.
soft_edge_format.remove()
# Kontrollera radien för den borttagna mjuka kanten.
self.assertEqual(0, soft_edge_format.radius)
```

### See Also

* module [aspose.words.drawing](../)

