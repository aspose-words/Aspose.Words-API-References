---
title: Adjustment.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "Adjustment.value property. Gets or sets the raw value of the adjustment."
type: docs
weight: 20
url: /python-net/aspose.words.model.drawing/adjustment/value/
---

## Adjustment.value property

Gets or sets the raw value of the adjustment.


```python
@property
def value(self) -> int:
    ...

@value.setter
def value(self, value: int):
    ...

```

### Remarks

An adjust value is simply a guide that has a value based formula specified.
That is, no calculation takes place for an adjust value guide.
Instead, this guide specifies a parameter value that is used for calculations within the shape guides.


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

* module [aspose.words.model.drawing](../../)
* class [Adjustment](../)

