---
title: GraphicsQualityOptions.SmoothingMode
linktitle: SmoothingMode
articleTitle: SmoothingMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SmoothingMode i GraphicsQualityOptions för att förbättra renderingskvaliteten och höja grafikprestanda utan ansträngning.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/graphicsqualityoptions/smoothingmode/
---
## GraphicsQualityOptions.SmoothingMode property

Hämtar eller ställer in renderingskvaliteten för denna grafik.

```csharp
public SmoothingMode? SmoothingMode { get; set; }
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
