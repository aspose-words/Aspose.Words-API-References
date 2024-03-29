---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words för .NET
description: GraphicsQualityOptions UseTileFlipMode fast egendom. Hämtar eller ställer in en flagga som indikerar om WrapMode är TileFlipXY i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Hämtar eller ställer in en flagga som indikerar om WrapMode är TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Anmärkningar

DeWrapMode anger hur en struktur eller gradient är sida vid sida när den är mindre än området som fylls.

Använder som standardTile (anger plattsättning utan att vända). Detta orsakar felaktig återgivning av den skalade bilden (med hög upplösning).

Den här egenskapen gör det möjligt att byta WrapMode tillTileFlipXY (anger att brickor vänds horisontellt när du flyttar längs en rad och vänds vertikalt när du flyttar längs en kolumn).

## Exempel

Visar hur man förhindrar att den vita linjen visas vid rendering med hög upplösning.

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

### Se även

* class [GraphicsQualityOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
