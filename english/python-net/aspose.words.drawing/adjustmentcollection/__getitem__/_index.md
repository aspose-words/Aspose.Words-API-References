---
title: AdjustmentCollection indexer
linktitle: AdjustmentCollection indexer
articleTitle: AdjustmentCollection indexer
second_title: Aspose.Words for Python
description: "AdjustmentCollection indexer. Returns an adjustment at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/adjustmentcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns an adjustment at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

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

