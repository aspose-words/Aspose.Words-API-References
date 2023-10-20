---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.GraphicsQualityOptions klass. Tillåter att ange ytterligareGraphics kvalitetsalternativ i C#.
type: docs
weight: 5040
url: /sv/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Tillåter att ange ytterligareGraphics kvalitetsalternativ.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class GraphicsQualityOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Hämtar eller ställer in ett värde som anger hur sammansatta bilder ritas till denna grafik. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritas till denna grafik. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Hämtar eller ställer in interpolationsläget som är associerat med denna grafik. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Hämtar eller ställer in renderingskvaliteten för denna grafik. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Hämtar eller ställer in information om textlayout (som justering, orientering och tabbstopp), visningsmanipulationer (som ellipsinsättning och nationell siffrorsättning) och OpenType-funktioner. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Hämtar eller ställer in renderingsläget för text som är associerad med denna grafik. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om WrapMode är TileFlipXY. |

## Exempel

Visar hur du ställer in alternativ för återgivningskvalitet när du konverterar dokument till bildformat.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
