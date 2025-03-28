---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words for .NET
description: Discover the GraphicsQualityOptions UseTileFlipMode property to control WrapMode settings for enhanced visual quality in your applications.
type: docs
weight: 80
url: /net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Gets or sets a flag indicating whether WrapMode is TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Remarks

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses Tile (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to TileFlipXY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

## Examples

Shows how to prevent the white line appears when rendering with a high resolution.

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### See Also

* class [GraphicsQualityOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
