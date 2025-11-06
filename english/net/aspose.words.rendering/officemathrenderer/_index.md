---
title: OfficeMathRenderer Class
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Rendering.OfficeMathRenderer class to effortlessly convert OfficeMath into stunning raster or vector images for your projects.
type: docs
weight: 5330
url: /net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

Provides methods to render an individual [`OfficeMath`](../../aspose.words.math/officemath/) to a raster or vector image or to a Graphics object.

To learn more, visit the [Working with OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) documentation article.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## Constructors

| Name | Description |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Gets the actual bounds of the shape in points. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Gets the opaque bounds of the shape in points. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Gets the actual size of the shape in points. |

## Methods

| Name | Description |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Renders the shape into a Graphics object to a specified scale. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Renders the shape into a Graphics object to a specified size. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renders the shape into an image and saves into a stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renders the shape into an SVG image and saves into a stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renders the shape into an image and saves into a file. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renders the shape into an SVG image and saves into a file. |

## Examples

Shows how to measure and scale shapes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
Assert.That(renderer.SizeInPoints.Width, Is.EqualTo(122.0f).Within(0.25f));
Assert.That(renderer.SizeInPoints.Height, Is.EqualTo(13.0f).Within(0.15f));

Assert.That(renderer.BoundsInPoints.Width, Is.EqualTo(122.0f).Within(0.25f));
Assert.That(renderer.BoundsInPoints.Height, Is.EqualTo(13.0f).Within(0.15f));

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
Assert.That(renderer.OpaqueBoundsInPoints.Width, Is.EqualTo(119.5f).Within(0.25f));
Assert.That(renderer.OpaqueBoundsInPoints.Height, Is.EqualTo(14.2f).Within(0.1f));

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);
string dpi96 = "DPI 96";
Assert.That(bounds.Width, Is.EqualTo(163), dpi96);
Assert.That(bounds.Height, Is.EqualTo(18), dpi96);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
string dpi96150 = "DPI 96 150";
Assert.That(bounds.Width, Is.EqualTo(163), dpi96150);
Assert.That(bounds.Height, Is.EqualTo(27), dpi96150);

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);
string dpi96Opaque = "DPI 96 Opaque";
Assert.That(bounds.Width, Is.EqualTo(160), dpi96Opaque);
Assert.That(bounds.Height, Is.EqualTo(19), dpi96Opaque);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
string dpi96150Opaque = "DPI 96 150 Opaque";
Assert.That(bounds.Width, Is.EqualTo(160), dpi96150Opaque);
Assert.That(bounds.Height, Is.EqualTo(29), dpi96150Opaque);
```

### See Also

* class [NodeRendererBase](../noderendererbase/)
* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
