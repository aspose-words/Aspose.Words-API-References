---
title: ShapeBase.is_decorative property
linktitle: is_decorative property
articleTitle: is_decorative property
second_title: Aspose.Words for Python
description: "ShapeBase.is_decorative property. Gets or sets the flag that specifies whether the shape is decorative in the document."
type: docs
weight: 240
url: /python-net/aspose.words.drawing/shapebase/is_decorative/
---

## ShapeBase.is_decorative property

Gets or sets the flag that specifies whether the shape is decorative in the document.


```python
@property
def is_decorative(self) -> bool:
    ...

@is_decorative.setter
def is_decorative(self, value: bool):
    ...

```

### Remarks

Note that shape having not empty [ShapeBase.alternative_text](../alternative_text/) cannot be decorative.



### Examples

Shows how to set that the shape is decorative.

```python
doc = aw.Document(MY_DIR + "Decorative shapes.docx")

shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(shape.is_decorative)

# If "alternative_text" is not empty, the shape cannot be decorative.
# That's why our value has changed to 'False'.
shape.alternative_text = "Alternative text."
self.assertFalse(shape.is_decorative)

builder = aw.DocumentBuilder(doc)

builder.move_to_document_end()
# Create a new shape as decorative.
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 100, 100)
shape.is_decorative = True

doc.save(ARTIFACTS_DIR + "Shape.is_decorative.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

