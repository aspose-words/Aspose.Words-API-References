---
title: Shape.fill_color property
linktitle: fill_color property
articleTitle: fill_color property
second_title: Aspose.Words for Python
description: "Shape.fill_color property. Defines the brush color that fills the closed path of the shape."
type: docs
weight: 50
url: /python-net/aspose.words.drawing/shape/fill_color/
---

## Shape.fill_color property

Defines the brush color that fills the closed path of the shape.


```python
@property
def fill_color(self) -> aspose.pydrawing.Color:
    ...

@fill_color.setter
def fill_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.white.





### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Write some text, and then cover it with a floating shape.
builder.font.size = 32
builder.writeln("Hello world!")

shape = builder.insert_shape(aw.drawing.ShapeType.CLOUD_CALLOUT, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 25,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 25, 250, 150, aw.drawing.WrapType.NONE)

# Use the "stroke_color" property to set the color of the outline of the shape.
shape.stroke_color = drawing.Color.cadet_blue

# Use the "fill_color" property to set the color of the inside area of the shape.
shape.fill_color = drawing.Color.light_blue

# The "opacity" property determines how transparent the color is on a 0-1 scale,
# with 1 being fully opaque, and 0 being invisible.
# The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
self.assertEqual(1.0, shape.fill.opacity)

# Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.fill.opacity = 0.3

doc.save(ARTIFACTS_DIR + "Shape.fill.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

