---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GraphicsQualityOptions UseTileFlipMode för att styra WrapMode-inställningar för förbättrad visuell kvalitet i dina applikationer.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Hämtar eller ställer in en flagga som anger om WrapMode är TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Anmärkningar

DeWrapMode anger hur en textur eller övertoning sida vid sida när den är mindre än det område som fylls.

Som standard använderTile (specificerar kakelplacering utan vändning). Detta orsakar felaktig återgivning av den skalade bilden (med hög upplösning).

Den här egenskapen tillåter att byta WrapMode tillTileFlipXY (specificerar att paneler vänds horisontellt när du förflyttar dig längs en rad och vänds vertikalt när du förflyttar dig längs en kolumn).

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
