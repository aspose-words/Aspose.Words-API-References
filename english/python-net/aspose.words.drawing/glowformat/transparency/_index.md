---
title: GlowFormat.transparency property
linktitle: transparency property
articleTitle: transparency property
second_title: Aspose.Words for Python
description: "GlowFormat.transparency property. Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear)"
type: docs
weight: 30
url: /python-net/aspose.words.drawing/glowformat/transparency/
---

## GlowFormat.transparency property

Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear).
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

