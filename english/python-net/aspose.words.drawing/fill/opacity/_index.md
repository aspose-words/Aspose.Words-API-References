---
title: Fill.opacity property
linktitle: opacity property
articleTitle: opacity property
second_title: Aspose.Words for Python
description: "Fill.opacity property. Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque)."
type: docs
weight: 150
url: /python-net/aspose.words.drawing/fill/opacity/
---

## Fill.opacity property

Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).


```python
@property
def opacity(self) -> float:
    ...

@opacity.setter
def opacity(self, value: float):
    ...

```

### Remarks

This property is the opposite of property [Fill.transparency](../transparency/).


### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Write some text, and then cover it with a floating shape.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Use the "StrokeColor" property to set the color of the outline of the shape.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Use the "FillColor" property to set the color of the inside area of the shape.
shape.fill_color = aspose.pydrawing.Color.light_blue
# The "Opacity" property determines how transparent the color is on a 0-1 scale,
# with 1 being fully opaque, and 0 being invisible.
# The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
self.assertEqual(1, shape.fill.opacity)
# Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

