---
title: ShadowFormat.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "ShadowFormat.type property. Gets or sets the specified [ShadowType](../../shadowtype/) for ShadowFormat."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/shadowformat/type/
---

## ShadowFormat.type property

Gets or sets the specified [ShadowType](../../shadowtype/) for ShadowFormat.



```python
@property
def type(self) -> aspose.words.drawing.ShadowType:
    ...

@type.setter
def type(self, value: aspose.words.drawing.ShadowType):
    ...

```

### Remarks

Setting a new shadow type will reset Color and Transparency values to their default ones.
Therefore, it makes sense to first set the desired shadow type and only then Color and Transparency values.


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
* class [ShadowFormat](../)

