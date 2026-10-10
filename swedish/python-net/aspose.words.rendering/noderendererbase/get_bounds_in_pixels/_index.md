---
title: NodeRendererBase.get_bounds_in_pixels method
linktitle: get_bounds_in_pixels method
articleTitle: get_bounds_in_pixels method
second_title: Aspose.Words for Python
description: "aspose.words.rendering.NodeRendererBase.get_bounds_in_pixels method"
type: docs
weight: 40
url: /sv/python-net/aspose.words.rendering/noderendererbase/get_bounds_in_pixels/
---

## get_bounds_in_pixels(scale, dpi) {#float_float}

Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.


```python
def get_bounds_in_pixels(self, scale: float, dpi: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

### Remarks

This method converts [NodeRendererBase.bounds_in_points](../bounds_in_points/) into rectangle in pixels.




### Returns

The actual (as rendered on the page) bounding box of the shape in pixels.


## get_bounds_in_pixels(scale, horizontal_dpi, vertical_dpi) {#float_float_float}

Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.


```python
def get_bounds_in_pixels(self, scale: float, horizontal_dpi: float, vertical_dpi: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontal_dpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| vertical_dpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

### Remarks

This method converts [NodeRendererBase.bounds_in_points](../bounds_in_points/) into rectangle in pixels.




### Returns

The actual (as rendered on the page) bounding box of the shape in pixels.


## Examples

Shows how to measure and scale shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
renderer = aw.rendering.OfficeMathRenderer(office_math)
# Verifiera storleken på bilden som OfficeMath‑objektet kommer att skapa när vi renderar den.
self.assertAlmostEqual(122, renderer.size_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.size_in_points.height, delta=0.15)
self.assertAlmostEqual(122, renderer.bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.bounds_in_points.height, delta=0.15)
# Former med transparenta delar kan innehålla olika värden i egenskaperna "OpaqueBoundsInPoints".
self.assertAlmostEqual(119.5, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)
# Hämta formens storlek i pixlar, med linjär skalning till en specifik DPI.
bounds = renderer.get_bounds_in_pixels(scale=1, dpi=96)
dpi96 = 'DPI 96'
self.assertEqual(163, bounds.width, msg=dpi96)
self.assertEqual(18, bounds.height, msg=dpi96)
# Hämta formens storlek i pixlar, men med en annan DPI för de horisontella och vertikala dimensionerna.
bounds = renderer.get_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi96150 = 'DPI 96 150'
self.assertEqual(163, bounds.width, msg=dpi96150)
self.assertEqual(27, bounds.height, msg=dpi96150)
# De ogenomskinliga gränserna kan också variera här.
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, dpi=96)
dpi_96_opaque = 'DPI 96 Opaque'
self.assertEqual(160, bounds.width, msg=dpi_96_opaque)
self.assertEqual(19, bounds.height, msg=dpi_96_opaque)
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi_96150_opaque = 'DPI 96 150 Opaque'
self.assertEqual(160, bounds.width, msg=dpi_96150_opaque)
self.assertEqual(29, bounds.height, msg=dpi_96150_opaque)
```

## See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

