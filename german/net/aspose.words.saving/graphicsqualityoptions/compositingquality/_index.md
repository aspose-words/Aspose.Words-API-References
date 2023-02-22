---
title: GraphicsQualityOptions.CompositingQuality
second_title: Aspose.Words für .NET-API-Referenz
description: GraphicsQualityOptions eigendom. Ruft die Renderqualität von zusammengesetzten Bildern ab die auf diese Grafik gezeichnet wurden oder legt sie fest.
type: docs
weight: 30
url: /de/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Ruft die Renderqualität von zusammengesetzten Bildern ab, die auf diese Grafik gezeichnet wurden, oder legt sie fest.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
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


