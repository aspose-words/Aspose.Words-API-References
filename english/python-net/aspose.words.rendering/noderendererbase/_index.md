---
title: NodeRendererBase class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/)."
type: docs
weight: 10
url: /python-net/aspose.words.rendering/noderendererbase/
---

## NodeRendererBase class

Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/).



### Properties

| Name | Description |
| --- | --- |
| [bounds_in_points](./bounds_in_points/) | Gets the actual bounds of the shape in points. |
| [opaque_bounds_in_points](./opaque_bounds_in_points/) | Gets the opaque bounds of the shape in points. |
| [size_in_points](./size_in_points/) | Gets the actual size of the shape in points. |

### Methods

| Name | Description |
| --- | --- |
|[ get_bounds_in_pixels(scale, dpi)](./get_bounds_in_pixels/#float_float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
|[ get_bounds_in_pixels(scale, horizontal_dpi, vertical_dpi)](./get_bounds_in_pixels/#float_float_float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
|[ get_opaque_bounds_in_pixels(scale, dpi)](./get_opaque_bounds_in_pixels/#float_float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
|[ get_opaque_bounds_in_pixels(scale, horizontal_dpi, vertical_dpi)](./get_opaque_bounds_in_pixels/#float_float_float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
|[ get_size_in_pixels(scale, dpi)](./get_size_in_pixels/#float_float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
|[ get_size_in_pixels(scale, horizontal_dpi, vertical_dpi)](./get_size_in_pixels/#float_float_float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
|[ save(file_name, save_options)](./save/#str_imagesaveoptions) | Renders the shape into an image and saves into a file. |
|[ save(stream, save_options)](./save/#bytesio_imagesaveoptions) | Renders the shape into an image and saves into a stream. |

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

* module [aspose.words.rendering](../)

