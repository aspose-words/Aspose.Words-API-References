---
title: NodeRendererBase.opaque_bounds_in_points property
linktitle: opaque_bounds_in_points property
articleTitle: opaque_bounds_in_points property
second_title: Aspose.Words for Python
description: "NodeRendererBase.opaque_bounds_in_points property. Gets the opaque bounds of the shape in points."
type: docs
weight: 20
url: /es/python-net/aspose.words.rendering/noderendererbase/opaque_bounds_in_points/
---

## NodeRendererBase.opaque_bounds_in_points property

Gets the opaque bounds of the shape in points.


```python
@property
def opaque_bounds_in_points(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Remarks

This property returns the opaque (i.e. transparent parts of the shape are ignored) bounding box of the shape.
The bounds takes the shape rotation into account.




### Examples

Shows how to measure and scale shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
renderer = aw.rendering.OfficeMathRenderer(office_math)
# Verifica el tamaño de la imagen que el objeto OfficeMath creará cuando lo rendericemos.
self.assertAlmostEqual(122, renderer.size_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.size_in_points.height, delta=0.15)
self.assertAlmostEqual(122, renderer.bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.bounds_in_points.height, delta=0.15)
# Las formas con partes transparentes pueden contener valores diferentes en las propiedades "OpaqueBoundsInPoints".
self.assertAlmostEqual(119.5, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)
# Obtén el tamaño de la forma en píxeles, con escalado lineal a un DPI específico.
bounds = renderer.get_bounds_in_pixels(scale=1, dpi=96)
dpi96 = 'DPI 96'
self.assertEqual(163, bounds.width, msg=dpi96)
self.assertEqual(18, bounds.height, msg=dpi96)
# Obtén el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontal y vertical.
bounds = renderer.get_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi96150 = 'DPI 96 150'
self.assertEqual(163, bounds.width, msg=dpi96150)
self.assertEqual(27, bounds.height, msg=dpi96150)
# Los límites opacos también pueden variar aquí.
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, dpi=96)
dpi_96_opaque = 'DPI 96 Opaque'
self.assertEqual(160, bounds.width, msg=dpi_96_opaque)
self.assertEqual(19, bounds.height, msg=dpi_96_opaque)
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi_96150_opaque = 'DPI 96 150 Opaque'
self.assertEqual(160, bounds.width, msg=dpi_96150_opaque)
self.assertEqual(29, bounds.height, msg=dpi_96150_opaque)
```

### See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

