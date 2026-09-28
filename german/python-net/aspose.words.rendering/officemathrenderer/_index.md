---
title: OfficeMathRenderer class
linktitle: OfficeMathRenderer class
articleTitle: OfficeMathRenderer class
second_title: Aspose.Words for Python
description: "aspose.words.rendering.OfficeMathRenderer class. Provides methods to render an individual [OfficeMath](../../aspose.words.math/officemath/) to a raster or vector image or to a Graphics object"
type: docs
weight: 20
url: /de/python-net/aspose.words.rendering/officemathrenderer/
---

## OfficeMathRenderer class

Provides methods to render an individual [OfficeMath](../../aspose.words.math/officemath/)
to a raster or vector image or to a Graphics object.
To learn more, visit the [Working with OfficeMath](https://docs.aspose.com/words/python-net/working-with-officemath/) documentation article.




**Inheritance:** [OfficeMathRenderer](./) → [NodeRendererBase](../noderendererbase/)

### Constructors
| Name | Description |
| --- | --- |
| [OfficeMathRenderer(math)](./__init__/#officemath) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [bounds_in_points](../noderendererbase/bounds_in_points/) | Gets the actual bounds of the shape in points.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
| [opaque_bounds_in_points](../noderendererbase/opaque_bounds_in_points/) | Gets the opaque bounds of the shape in points.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
| [size_in_points](../noderendererbase/size_in_points/) | Gets the actual size of the shape in points.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_bounds_in_pixels(scale, dpi)](../noderendererbase/get_bounds_in_pixels/#float_float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ get_bounds_in_pixels(scale, horizontal_dpi, vertical_dpi)](../noderendererbase/get_bounds_in_pixels/#float_float_float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ get_opaque_bounds_in_pixels(scale, dpi)](../noderendererbase/get_opaque_bounds_in_pixels/#float_float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ get_opaque_bounds_in_pixels(scale, horizontal_dpi, vertical_dpi)](../noderendererbase/get_opaque_bounds_in_pixels/#float_float_float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ get_size_in_pixels(scale, dpi)](../noderendererbase/get_size_in_pixels/#float_float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ get_size_in_pixels(scale, horizontal_dpi, vertical_dpi)](../noderendererbase/get_size_in_pixels/#float_float_float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(file_name, save_options)](../noderendererbase/save/#str_imagesaveoptions) | Renders the shape into an image and saves into a file.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(file_name, save_options)](../noderendererbase/save/#str_svgsaveoptions) | Renders the shape into an SVG image and saves into a file.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(stream, save_options)](../noderendererbase/save/#bytesio_imagesaveoptions) | Renders the shape into an image and saves into a stream.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(stream, save_options)](../noderendererbase/save/#bytesio_svgsaveoptions) | Renders the shape into an SVG image and saves into a stream.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |

### Examples

Shows how to measure and scale shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
renderer = aw.rendering.OfficeMathRenderer(office_math)
# Überprüfen Sie die Größe des Bildes, das das OfficeMath-Objekt beim Rendern erzeugt.
self.assertAlmostEqual(122, renderer.size_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.size_in_points.height, delta=0.15)
self.assertAlmostEqual(122, renderer.bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(13, renderer.bounds_in_points.height, delta=0.15)
# Formen mit transparenten Teilen können unterschiedliche Werte in den "OpaqueBoundsInPoints"-Eigenschaften enthalten.
self.assertAlmostEqual(119.5, renderer.opaque_bounds_in_points.width, delta=0.25)
self.assertAlmostEqual(14.2, renderer.opaque_bounds_in_points.height, delta=0.1)
# Ermitteln Sie die Formgröße in Pixeln, mit linearer Skalierung auf einen bestimmten DPI.
bounds = renderer.get_bounds_in_pixels(scale=1, dpi=96)
dpi96 = 'DPI 96'
self.assertEqual(163, bounds.width, msg=dpi96)
self.assertEqual(18, bounds.height, msg=dpi96)
# Ermitteln Sie die Formgröße in Pixeln, jedoch mit einem anderen DPI für die horizontale und vertikale Dimension.
bounds = renderer.get_bounds_in_pixels(scale=1, horizontal_dpi=96, vertical_dpi=150)
dpi96150 = 'DPI 96 150'
self.assertEqual(163, bounds.width, msg=dpi96150)
self.assertEqual(27, bounds.height, msg=dpi96150)
# Die undurchsichtigen Grenzen können hier ebenfalls variieren.
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
* class [NodeRendererBase](../noderendererbase/)

