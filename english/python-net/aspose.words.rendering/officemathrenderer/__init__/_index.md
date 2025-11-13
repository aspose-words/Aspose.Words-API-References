---
title: OfficeMathRenderer constructor
linktitle: OfficeMathRenderer constructor
articleTitle: OfficeMathRenderer constructor
second_title: Aspose.Words for Python
description: "OfficeMathRenderer constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /python-net/aspose.words.rendering/officemathrenderer/__init__/
---

## OfficeMathRenderer(math) {#officemath}

Initializes a new instance of this class.


```python
def __init__(self, math: aspose.words.math.OfficeMath):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| math | [OfficeMath](../../../aspose.words.math/officemath/) | The [OfficeMath](../../../aspose.words.math/officemath/) object that you want to render. |

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
self.assertAlmostEqual(119.5, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)
# Get the shape size in pixels, with linear scaling to a specific DPI.
bounds = renderer.get_bounds_in_pixels(scale=1, dpi=96)
dpi96 = 'DPI 96'
self.assertEqual(163, bounds.width, msg=dpi96)
self.assertEqual(18, bounds.height, msg=dpi96)
# Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.get_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi96150 = 'DPI 96 150'
self.assertEqual(163, bounds.width, msg=dpi96150)
self.assertEqual(27, bounds.height, msg=dpi96150)
# The opaque bounds may vary here also.
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
* class [OfficeMathRenderer](../)

