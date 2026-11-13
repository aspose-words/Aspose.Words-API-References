---
title: GradientStop constructor
linktitle: GradientStop constructor
articleTitle: GradientStop constructor
second_title: Aspose.Words for Python
description: "aspose.words.drawing.GradientStop constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words.drawing/gradientstop/__init__/
---

## GradientStop(color, position) {#color_float}

Initializes a new instance of the [GradientStop](../) class.



```python
def __init__(self, color: aspose.pydrawing.Color, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| color | aspose.pydrawing.Color | Represents the color of the gradient stop. |
| position | float | Represents the position of a stop within the gradient expressed as a percent in range 0.0 to 1.0. |

## GradientStop(color, position, transparency) {#color_float_float}

Initializes a new instance of the [GradientStop](../) class.



```python
def __init__(self, color: aspose.pydrawing.Color, position: float, transparency: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| color | aspose.pydrawing.Color | Represents the color of the gradient stop. |
| position | float | Represents the position of a stop within the gradient expressed as a percent in range 0.0 to 1.0. |
| transparency | float | Represents the transparency of a stop within the gradient expressed as a percent in range 0.0 to 1.0. |

## Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# Obtenga la colección de paradas de degradado.
gradient_stops = shape.fill.gradient_stops
# Cambie la primera parada de degradado.
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# Añada una nueva parada de degradado al final de la colección.
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# Elimine la parada de degradado en el índice 1.
gradient_stops.remove_at(1)
# E inserte una nueva parada de degradado en el mismo índice 1.
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# Eliminar el último punto de degradado en la colección.
gradient_stop = gradient_stops[2]
gradient_stops.remove(gradient_stop)
self.assertEqual(2, gradient_stops.count)
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 0, 255, 255), gradient_stops[0].base_color)
self.assertEqual(aspose.pydrawing.Color.aqua.to_argb(), gradient_stops[0].color.to_argb())
self.assertAlmostEqual(0.1, gradient_stops[0].position, delta=0.01)
self.assertAlmostEqual(0.25, gradient_stops[0].transparency, delta=0.01)
self.assertEqual(aspose.pydrawing.Color.chocolate.to_argb(), gradient_stops[1].color.to_argb())
self.assertAlmostEqual(0.75, gradient_stops[1].position, delta=0.01)
self.assertAlmostEqual(0.3, gradient_stops[1].transparency, delta=0.01)
# Utilice la opción de cumplimiento para definir la forma usando DML
# si desea obtener la propiedad "GradientStops" después de que el documento se guarde.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

## See Also

* module [aspose.words.drawing](../../)
* class [GradientStop](../)

