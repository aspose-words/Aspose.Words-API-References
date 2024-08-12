---
title: GlowFormat class
linktitle: GlowFormat class
articleTitle: GlowFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.GlowFormat class. Represents the glow formatting for an object."
type: docs
weight: 110
url: /python-net/aspose.words.drawing/glowformat/
---

## GlowFormat class

Represents the glow formatting for an object.


### Remarks

Use the [ShapeBase.glow](../shapebase/glow/) property to access glow properties of an object.
You do not create instances of the [GlowFormat](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets a aspose.pydrawing.Color object that represents the color for a glow effect. The default value is aspose.pydrawing.Color.black. |
| [radius](./radius/) | Gets or sets a double value that represents the length of the radius for a glow effect in points (pt). The default value is 0.0. |
| [transparency](./transparency/) | Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes [GlowFormat](./) from the parent object. |

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

* module [aspose.words.drawing](../)

