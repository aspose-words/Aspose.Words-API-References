---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Rendering.NodeRendererBase class—your foundation for efficient Shape and OfficeMath rendering in document processing.
type: docs
weight: 5310
url: /net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Base class for [`ShapeRenderer`](../shaperenderer/) and [`OfficeMathRenderer`](../officemathrenderer/).

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public abstract class NodeRendererBase
```

## Properties

| Name | Description |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Gets the actual bounds of the shape in points. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Gets the opaque bounds of the shape in points. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Gets the actual size of the shape in points. |

## Methods

| Name | Description |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Renders the shape into a Graphics object to a specified scale. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Renders the shape into a Graphics object to a specified size. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renders the shape into an image and saves into a stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renders the shape into an SVG image and saves into a stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renders the shape into an image and saves into a file. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renders the shape into an SVG image and saves into a file. |

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
Assert.That(renderer.OpaqueBoundsInPoints.Width, Is.EqualTo(122.0f).Within(0.25f));
Assert.That(renderer.OpaqueBoundsInPoints.Height, Is.EqualTo(14.2f).Within(0.1f));

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.That(bounds.Width, Is.EqualTo(163));
Assert.That(bounds.Height, Is.EqualTo(18));

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.That(bounds.Width, Is.EqualTo(163));
Assert.That(bounds.Height, Is.EqualTo(27));

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.That(bounds.Width, Is.EqualTo(163));
Assert.That(bounds.Height, Is.EqualTo(19));

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.That(bounds.Width, Is.EqualTo(163));
Assert.That(bounds.Height, Is.EqualTo(29));
```

### See Also

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
