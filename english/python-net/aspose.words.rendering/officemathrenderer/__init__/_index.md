﻿---
title: OfficeMathRenderer constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "Initializes a new instance of this class."
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
| math | [OfficeMath](../../../aspose.words.math/officemath/) |  |

### Examples

Shows how to measure and scale shapes.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
renderer = aw.rendering.OfficeMathRenderer(office_math)

# Verify the size of the image that the OfficeMath object will create when we render it.
self.assertAlmostEqual(119.0, renderer.size_in_points.width, delta=0.2)
self.assertAlmostEqual(13.0, renderer.size_in_points.height, delta=0.1)

self.assertAlmostEqual(119.0, renderer.bounds_in_points.width, delta=0.2)
self.assertAlmostEqual(13.0, renderer.bounds_in_points.height, delta=0.1)

# Shapes with transparent parts may contain different values in the "opaque_bounds_in_points" properties.
self.assertAlmostEqual(119.0, renderer.opaque_bounds_in_points.width, delta=0.2)
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

### See Also

* module [aspose.words.rendering](../../)
* class [OfficeMathRenderer](../)
