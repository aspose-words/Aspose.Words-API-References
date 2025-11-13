---
title: NodeRendererBase class
linktitle: NodeRendererBase class
articleTitle: NodeRendererBase class
second_title: Aspose.Words for Python
description: "aspose.words.rendering.NodeRendererBase class. Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/)"
type: docs
weight: 10
url: /python-net/aspose.words.rendering/noderendererbase/
---

## NodeRendererBase class

Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/).
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




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
|[ save(file_name, save_options)](./save/#str_svgsaveoptions) | Renders the shape into an SVG image and saves into a file. |
|[ save(stream, save_options)](./save/#bytesio_imagesaveoptions) | Renders the shape into an image and saves into a stream. |
|[ save(stream, save_options)](./save/#bytesio_svgsaveoptions) | Renders the shape into an SVG image and saves into a stream. |

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

* module [aspose.words.rendering](../)

