---
title: AdjustmentCollection class
linktitle: AdjustmentCollection class
articleTitle: AdjustmentCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.AdjustmentCollection class. Represents a read-only collection of [Adjustment](../adjustment/) adjust values that are applied to the specified shape."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/adjustmentcollection/
---

## AdjustmentCollection class

Represents a read-only collection of [Adjustment](../adjustment/) adjust values that are applied to the specified shape.



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns an adjustment at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

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

* module [aspose.words.drawing](../)

