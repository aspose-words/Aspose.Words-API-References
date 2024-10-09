---
title: ShapeBase.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "ShapeBase.hidden property. Gets or sets a boolean value indicating whether the shape is visible."
type: docs
weight: 230
url: /python-net/aspose.words.drawing/shapebase/hidden/
---

## ShapeBase.hidden property

Gets or sets a boolean value indicating whether the shape is visible.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.



### Examples

Shows how to hide the shape.

```python
doc = aw.Document(file_name=MY_DIR + 'Shadow color.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
if not shape.hidden:
    shape.hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Hidden.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

