---
title: GlowFormat.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "GlowFormat.color property. Gets or sets a aspose.pydrawing.Color object that represents the color for a glow effect"
type: docs
weight: 10
url: /python-net/aspose.words.drawing/glowformat/color/
---

## GlowFormat.color property

Gets or sets a aspose.pydrawing.Color object that represents the color for a glow effect.
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

Shows how to interact with glow shape effect.

```python
doc = aw.Document(file_name=MY_DIR + "Various shapes.docx")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shape.glow.color = aspose.pydrawing.Color.salmon
shape.glow.radius = 30
shape.glow.transparency = 0.15
doc.save(file_name=ARTIFACTS_DIR + "Shape.Glow.docx")
doc = aw.Document(file_name=ARTIFACTS_DIR + "Shape.Glow.docx")
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

