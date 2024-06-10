---
title: ShadowFormat.visible property
linktitle: visible property
articleTitle: visible property
second_title: Aspose.Words for Python
description: "ShadowFormat.visible property. Returns ``True`` if the formatting applied to this instance is visible."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/shadowformat/visible/
---

## ShadowFormat.visible property

Returns ``True`` if the formatting applied to this instance is visible.



```python
@property
def visible(self) -> bool:
    ...

```

### Remarks

Unlike [ShadowFormat.clear()](../clear/#default), assigning ``False`` to Visible does not clear the formatting,
it only hides the shape effect.



### Examples

Shows how to work with a shadow formatting for the shape.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape stroke pattern border.docx')
shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
if shape.shadow_format.visible and shape.shadow_format.type == aw.drawing.ShadowType.SHADOW2:
    shape.shadow_format.type = aw.drawing.ShadowType.SHADOW7
if shape.shadow_format.type == aw.drawing.ShadowType.SHADOW_MIXED:
    shape.shadow_format.clear()
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShadowFormat](../)

