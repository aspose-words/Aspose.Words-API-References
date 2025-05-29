---
title: GraphicsQualityOptions.InterpolationMode
linktitle: InterpolationMode
articleTitle: InterpolationMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GraphicsQualityOptions InterpolationMode för att enkelt anpassa grafikens interpoleringsinställningar för förbättrad visuell kvalitet.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Hämtar eller ställer in interpoleringsläget som är associerat med denna grafik.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
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
