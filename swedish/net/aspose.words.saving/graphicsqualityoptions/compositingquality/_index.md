---
title: GraphicsQualityOptions.CompositingQuality
linktitle: CompositingQuality
articleTitle: CompositingQuality
second_title: Aspose.Words för .NET
description: GraphicsQualityOptions CompositingQuality fast egendom. Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritas till denna grafik i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritas till denna grafik.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

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

* class [GraphicsQualityOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
