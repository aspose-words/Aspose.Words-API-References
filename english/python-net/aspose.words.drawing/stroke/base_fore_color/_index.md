---
title: Stroke.base_fore_color property
linktitle: base_fore_color property
articleTitle: base_fore_color property
second_title: Aspose.Words for Python
description: "Stroke.base_fore_color property. Gets the base foreground color of the stroke without any modifiers."
type: docs
weight: 20
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
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 100, 40)
shape.fill.fore_color = drawing.Color.red
shape.fill.fore_tint_and_shade = 0.5
shape.stroke.fill.fore_color = drawing.Color.green
shape.stroke.fill.transparency = 0.5
drawing.Color.from_argb(255, 255, 188, 188).to_argb()

self.assertEqual(drawing.Color.from_argb(255, 255, 188, 188).to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(drawing.Color.red.to_argb(), shape.fill.base_fore_color.to_argb())
self.assertEqual(drawing.Color.from_argb(128, 0, 128, 0).to_argb(), shape.stroke.fore_color.to_argb())
self.assertEqual(drawing.Color.green.to_argb(), shape.stroke.base_fore_color.to_argb())

self.assertEqual(drawing.Color.green.to_argb(), shape.stroke.fill.fore_color.to_argb())
self.assertEqual(drawing.Color.green.to_argb(), shape.stroke.fill.base_fore_color.to_argb())
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

