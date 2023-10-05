---
title: ShapeRenderer Class
linktitle: ShapeRenderer
articleTitle: ShapeRenderer
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.ShapeRenderer class. Provides methods to render an individual Shape or GroupShape to a raster or vector image or to a Graphics object in C#.
type: docs
weight: 4590
url: /net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

Provides methods to render an individual [`Shape`](../../aspose.words.drawing/shape/) or [`GroupShape`](../../aspose.words.drawing/groupshape/) to a raster or vector image or to a Graphics object.

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## Constructors

| Name | Description |
| --- | --- |
| [ShapeRenderer](shaperenderer/)(*[ShapeBase](../../aspose.words.drawing/shapebase/)*) |  |

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
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renders the shape into an image and saves into a file. |

### See Also

* class [NodeRendererBase](../noderendererbase/)
* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
