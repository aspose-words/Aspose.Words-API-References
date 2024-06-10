---
title: ShadowFormat.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "ShadowFormat.color property. Gets a aspose.pydrawing.Color object that represents the color for the shadow"
type: docs
weight: 10
url: /python-net/aspose.words.drawing/shadowformat/color/
---

## ShadowFormat.color property

Gets a aspose.pydrawing.Color object that represents the color for the shadow.
The default value is aspose.pydrawing.Color.black.



```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

```

### Examples

Shows how to get shadow color.

```python
doc = aw.Document(file_name=MY_DIR + 'Shadow color.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.shadow_format.color.to_argb())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShadowFormat](../)

