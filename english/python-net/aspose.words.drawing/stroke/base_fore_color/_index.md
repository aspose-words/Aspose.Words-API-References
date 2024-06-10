---
title: Stroke.base_fore_color property
linktitle: base_fore_color property
articleTitle: base_fore_color property
second_title: Aspose.Words for Python
description: "Stroke.base_fore_color property. Gets the base foreground color of the stroke without any modifiers."
type: docs
weight: 40
url: /python-net/aspose.words.drawing/stroke/base_fore_color/
---

## Stroke.base_fore_color property

Gets the base foreground color of the stroke without any modifiers.


```python
@property
def base_fore_color(self) -> aspose.pydrawing.Color:
    ...

```

### Remarks

The default value for a [Shape](../../shape/) is
aspose.pydrawing.Color.black.



### Examples

Shows how to get foreground color without modifiers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder()
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
shape.fill.fore_color = aspose.pydrawing.Color.red
shape.fill.fore_tint_and_shade = 0.5
shape.stroke.fill.fore_color = aspose.pydrawing.Color.green
shape.stroke.fill.transparency = 0.5
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 255, 188, 188).to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.base_fore_color.to_argb())
self.assertEqual(aspose.pydrawing.Color.from_argb(128, 0, 128, 0).to_argb(), shape.stroke.fore_color.to_argb())
self.assertEqual(aspose.pydrawing.Color.green.to_argb(), shape.stroke.base_fore_color.to_argb())
self.assertEqual(aspose.pydrawing.Color.green.to_argb(), shape.stroke.fill.fore_color.to_argb())
self.assertEqual(aspose.pydrawing.Color.green.to_argb(), shape.stroke.fill.base_fore_color.to_argb())
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

