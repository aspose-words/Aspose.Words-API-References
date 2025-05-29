---
title: GraphicsQualityOptions.CompositingQuality
linktitle: CompositingQuality
articleTitle: CompositingQuality
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GraphicsQualityOptions CompositingQuality för att förbättra din bildrendering. Optimera sammansatta bilder för enastående visuell kvalitet!
type: docs
weight: 30
url: /sv/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Hämtar eller ställer in renderingskvaliteten för sammansatta bilder som ritats till denna grafik.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

## Exempel

Visar hur man ställer in alternativ för renderingskvalitet vid konvertering av dokument till bildformat.

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
