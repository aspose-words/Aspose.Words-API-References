---
title: Shape.stroke_color property
linktitle: stroke_color property
articleTitle: stroke_color property
second_title: Aspose.Words for Python
description: "Shape.stroke_color property. Defines the color of a stroke."
type: docs
weight: 200
url: /es/python-net/aspose.words.drawing/shape/stroke_color/
---

## Shape.stroke_color property

Defines the color of a stroke.


```python
@property
def stroke_color(self) -> aspose.pydrawing.Color:
    ...

@stroke_color.setter
def stroke_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Stroke.color](../../stroke/color/) property.

The default value is
aspose.pydrawing.Color.black.





### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Escribe algún texto y luego cúbrelo con una forma flotante.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Utiliza la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Utiliza la propiedad "FillColor" para establecer el color del área interior de la forma.
shape.fill_color = aspose.pydrawing.Color.light_blue
# La propiedad "Opacity" determina cuán transparente es el color en una escala de 0 a 1,
# siendo 1 totalmente opaco y 0 invisible.
# El relleno de la forma por defecto es totalmente opaco, por lo que no podemos ver el texto que está debajo de esta forma.
self.assertEqual(1, shape.fill.opacity)
# Establece la opacidad del color de relleno de la forma a un valor más bajo para que podamos ver el texto debajo de ella.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

