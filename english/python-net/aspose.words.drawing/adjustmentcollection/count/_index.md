---
title: AdjustmentCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "AdjustmentCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/adjustmentcollection/count/
---

## AdjustmentCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
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
* class [AdjustmentCollection](../)

