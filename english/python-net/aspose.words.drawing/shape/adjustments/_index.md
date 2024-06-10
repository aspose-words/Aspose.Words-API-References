---
title: Shape.adjustments property
linktitle: adjustments property
articleTitle: adjustments property
second_title: Aspose.Words for Python
description: "Shape.adjustments property. Provides access to the adjustment raw values of a shape"
type: docs
weight: 20
url: /python-net/aspose.words.drawing/shape/adjustments/
---

## Shape.adjustments property

Provides access to the adjustment raw values of a shape.
For a shape that does not contain any adjustment raw values, it returns an empty collection.


```python
@property
def adjustments(self) -> aspose.words.drawing.AdjustmentCollection:
    ...

```

### Examples

Shows how to work with adjustment raw values.

```python
doc = aw.Document(file_name=MY_DIR + 'Rounded rectangle shape.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
adjustments = shape.adjustments
self.assertEqual(1, adjustments.count)
adjustment = adjustments[0]
self.assertEqual('adj', adjustment.name)
self.assertEqual(16667, adjustment.value)
adjustment.value = 30000
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Adjustments.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

