---
title: ShadowFormat.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "ShadowFormat.color property. Gets or sets a aspose.pydrawing.Color object that represents the color for the shadow"
type: docs
weight: 10
url: /python-net/aspose.words.drawing/shadowformat/color/
---

## ShadowFormat.color property

Gets or sets a aspose.pydrawing.Color object that represents the color for the shadow.
The default value is aspose.pydrawing.Color.black.



```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
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

Shows how to set a color with transparency.

```python
doc = aw.Document(file_name=MY_DIR + 'Shadow color.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shadow_format = shape.shadow_format
shadow_format.type = aw.drawing.ShadowType.SHADOW21
shadow_format.color = aspose.pydrawing.Color.red
shadow_format.transparency = 0.8
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ShadowFormatTransparency.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShadowFormat](../)

