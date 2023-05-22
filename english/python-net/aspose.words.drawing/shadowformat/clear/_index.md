---
title: ShadowFormat.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ShadowFormat.clear method. Clears shadow format."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/shadowformat/clear/
---

## clear() {#default}

Clears shadow format.


```python
def clear(self):
    ...
```

### Examples

Shows how to work with a shadow formatting for the shape.

```python
doc = aw.Document(MY_DIR + "Shape stroke pattern border.docx")
shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
if shape.shadow_format.visible and shape.shadow_format.type == awd.ShadowType.SHADOW2:
    shape.shadow_format.type == awd.ShadowType.SHADOW7
if shape.shadow_format.type == awd.ShadowType.SHADOW_MIXED:
    shape.shadow_format.clear()
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShadowFormat](../)

