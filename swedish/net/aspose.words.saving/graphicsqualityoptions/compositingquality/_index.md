---
title: GraphicsQualityOptions.CompositingQuality
second_title: Aspose.Words för .NET API Referens
description: GraphicsQualityOptions fast egendom. Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritas till denna grafik.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritas till denna grafik.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words.Saving](../../graphicsqualityoptions/)
* hopsättning [Aspose.Words](../../../)


