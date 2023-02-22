---
title: GraphicsQualityOptions.CompositingMode
second_title: Aspose.Words för .NET API Referens
description: GraphicsQualityOptions fast egendom. Hämtar eller ställer in ett värde som anger hur sammansatta bilder ritas till denna grafik.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Hämtar eller ställer in ett värde som anger hur sammansatta bilder ritas till denna grafik.

```csharp
public CompositingMode? CompositingMode { get; set; }
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


