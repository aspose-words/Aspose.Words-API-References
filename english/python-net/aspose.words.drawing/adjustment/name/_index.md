---
title: Adjustment.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Adjustment.name property. Gets the name of the adjustment."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/adjustment/name/
---

## Adjustment.name property

Gets the name of the adjustment.


```python
@property
def name(self) -> str:
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
* class [Adjustment](../)

