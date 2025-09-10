---
title: ShadowFormat.transparency property
linktitle: transparency property
articleTitle: transparency property
second_title: Aspose.Words for Python
description: "ShadowFormat.transparency property. Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear)"
type: docs
weight: 20
url: /python-net/aspose.words.drawing/shadowformat/transparency/
---

## ShadowFormat.transparency property

Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear).
The default value is 0.0.


```python
@property
def transparency(self) -> float:
    ...

@transparency.setter
def transparency(self, value: float):
    ...

```

### Examples

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

