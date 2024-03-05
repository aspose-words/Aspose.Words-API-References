---
title: NodeRendererBase.get_bounds_in_pixels method
linktitle: get_bounds_in_pixels method
articleTitle: get_bounds_in_pixels method
second_title: Aspose.Words for Python
description: "aspose.words.rendering.NodeRendererBase.get_bounds_in_pixels method"
type: docs
weight: 40
url: /python-net/aspose.words.rendering/noderendererbase/get_bounds_in_pixels/
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
doc = aw.Document(MY_DIR + "Office math.docx")

office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
renderer = aw.rendering.OfficeMathRenderer(office_math)

# Verify the size of the image that the OfficeMath object will create when we render it.
self.assertAlmostEqual(119.0, renderer.size_in_points.width, delta=0.25)
self.assertAlmostEqual(13.0, renderer.size_in_points.height, delta=0.1)

self.assertAlmostEqual(119.0, renderer.bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(13.0, renderer.bounds_in_points.height, delta=0.1)

# Shapes with transparent parts may contain different values in the "opaque_bounds_in_points" properties.
self.assertAlmostEqual(119.0, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)

# Get the shape size in pixels, with linear scaling to a specific DPI.
bounds = renderer.get_bounds_in_pixels(1.0, 96.0)

self.assertEqual(159, bounds.width)
self.assertEqual(18, bounds.height)

# Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.get_bounds_in_pixels(1.0, 96.0, 150.0)
self.assertEqual(159, bounds.width)
self.assertEqual(28, bounds.height)

# The opaque bounds may vary here also.
bounds = renderer.get_opaque_bounds_in_pixels(1.0, 96.0)

self.assertEqual(159, bounds.width)
self.assertEqual(18, bounds.height)

bounds = renderer.get_opaque_bounds_in_pixels(1.0, 96.0, 150.0)

self.assertEqual(159, bounds.width)
self.assertEqual(30, bounds.height)
```

## See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

