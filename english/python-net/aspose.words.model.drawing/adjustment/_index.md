---
title: Adjustment class
linktitle: Adjustment class
articleTitle: Adjustment class
second_title: Aspose.Words for Python
description: "aspose.words.model.drawing.Adjustment class. Represents adjustment values that are applied to the specified shape."
type: docs
weight: 10
url: /python-net/aspose.words.model.drawing/adjustment/
---

## Adjustment class

Represents adjustment values that are applied to the specified shape.


### Properties

| Name | Description |
| --- | --- |
| [name](./name/) | Gets the name of the adjustment. |
| [value](./value/) | Gets or sets the raw value of the adjustment. |

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

* module [aspose.words.model.drawing](../)

