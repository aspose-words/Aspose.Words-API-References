---
title: GraphicsQualityOptions.InterpolationMode
second_title: Aspose.Words für .NET-API-Referenz
description: GraphicsQualityOptions eigendom. Ruft den mit dieser Grafik verknüpften Interpolationsmodus ab oder legt ihn fest.
type: docs
weight: 40
url: /de/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Ruft den mit dieser Grafik verknüpften Interpolationsmodus ab oder legt ihn fest.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

### Beispiele

Zeigt, wie Optionen für die Renderqualität beim Konvertieren von Dokumenten in Bildformate festgelegt werden.

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

### Siehe auch

* class [GraphicsQualityOptions](../)
* namensraum [Aspose.Words.Saving](../../graphicsqualityoptions/)
* Montage [Aspose.Words](../../../)


