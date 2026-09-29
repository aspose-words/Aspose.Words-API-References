---
title: Fill.opacity property
linktitle: opacity property
articleTitle: opacity property
second_title: Aspose.Words for Python
description: "Fill.opacity property. Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque)."
type: docs
weight: 150
url: /sv/python-net/aspose.words.drawing/fill/opacity/
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
# Skriv lite text och täck sedan den med en flytande form.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Använd egenskapen "StrokeColor" för att sätta färgen på formens kontur.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Använd egenskapen "FillColor" för att sätta färgen på formens insida.
shape.fill_color = aspose.pydrawing.Color.light_blue
# "Opacity"-egenskapen bestämmer hur genomskinlig färgen är på en skala från 0 till 1,
# där 1 är helt ogenomskinlig och 0 är osynlig.
# Formens fyllning är som standard helt ogenomskinlig, så vi kan inte se texten som den ligger ovanpå.
self.assertEqual(1, shape.fill.opacity)
# Sätt formens fyllningsfärgs opacitet till ett lägre värde så att vi kan se texten under den.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

