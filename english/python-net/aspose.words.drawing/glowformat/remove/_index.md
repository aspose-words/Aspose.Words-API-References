---
title: GlowFormat.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "GlowFormat.remove method. Removes [GlowFormat](../) from the parent object."
type: docs
weight: 40
url: /python-net/aspose.words.drawing/glowformat/remove/
---

## remove() {#default}

Removes [GlowFormat](../) from the parent object.



```python
def remove(self):
    ...
```

### Examples

Shows how to interact with glow shape effect.

```python
doc = aw.Document(file_name=MY_DIR + 'Various shapes.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shape.glow.color = aspose.pydrawing.Color.salmon
shape.glow.radius = 30
shape.glow.transparency = 0.15
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Glow.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.Glow.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(aspose.pydrawing.Color.from_argb(217, 250, 128, 114).to_argb(), shape.glow.color.to_argb())
self.assertEqual(30, shape.glow.radius)
self.assertAlmostEqual(0.15, shape.glow.transparency, delta=0.01)
shape.glow.remove()
self.assertEqual(aspose.pydrawing.Color.black.to_argb(), shape.glow.color.to_argb())
self.assertEqual(0, shape.glow.radius)
self.assertEqual(0, shape.glow.transparency)
```

### See Also

* module [aspose.words.drawing](../../)
* class [GlowFormat](../)

