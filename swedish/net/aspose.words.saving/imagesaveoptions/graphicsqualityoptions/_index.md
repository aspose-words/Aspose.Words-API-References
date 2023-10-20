---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words för .NET
description: ImageSaveOptions GraphicsQualityOptions fast egendom. Tillåter att ange renderingsläge och kvalitet förGraphics objekt i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Tillåter att ange renderingsläge och kvalitet förGraphics objekt.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Anmärkningar

Använd den här egenskapen för att åsidosätta grafikinställningarna som tillhandahålls av Aspose.Words-motorn som standard.

Det träder i kraft endast när ett dokument sparas i ett bildliknande format.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
