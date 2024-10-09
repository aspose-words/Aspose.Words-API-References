---
title: ShapeBase.shadow_format property
linktitle: shadow_format property
articleTitle: shadow_format property
second_title: Aspose.Words for Python
description: "ShapeBase.shadow_format property. Gets shadow formatting for the shape."
type: docs
weight: 520
url: /python-net/aspose.words.drawing/shapebase/shadow_format/
---

## ShapeBase.shadow_format property

Gets shadow formatting for the shape.


```python
@property
def shadow_format(self) -> aspose.words.drawing.ShadowFormat:
    ...

```

### Examples

Shows how to get shadow color.

```python
doc = aw.Document(file_name=MY_DIR + 'Shadow color.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shadow_format = shape.shadow_format
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shadow_format.color.to_argb())
self.assertEqual(aw.drawing.ShadowType.SHADOW_MIXED, shadow_format.type)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

