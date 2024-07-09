---
title: NodeRendererBase.opaque_bounds_in_points property
linktitle: opaque_bounds_in_points property
articleTitle: opaque_bounds_in_points property
second_title: Aspose.Words for Python
description: "NodeRendererBase.opaque_bounds_in_points property. Gets the opaque bounds of the shape in points."
type: docs
weight: 20
url: /python-net/aspose.words.rendering/noderendererbase/opaque_bounds_in_points/
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
# Verify the size of the image that the OfficeMath object will create when we render it.
self.assertAlmostEqual(122, renderer.size_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.size_in_points.height, delta=0.15)
self.assertAlmostEqual(122, renderer.bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.bounds_in_points.height, delta=0.15)
# Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
self.assertAlmostEqual(122, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)
# Get the shape size in pixels, with linear scaling to a specific DPI.
bounds = renderer.get_bounds_in_pixels(scale=1, dpi=96)
self.assertEqual(163, bounds.width)
self.assertEqual(18, bounds.height)
# Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.get_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
self.assertEqual(163, bounds.width)
self.assertEqual(27, bounds.height)
# The opaque bounds may vary here also.
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, dpi=96)
self.assertEqual(163, bounds.width)
self.assertEqual(19, bounds.height)
bounds = renderer.get_opaque_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
self.assertEqual(163, bounds.width)
self.assertEqual(29, bounds.height)
```

### See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

