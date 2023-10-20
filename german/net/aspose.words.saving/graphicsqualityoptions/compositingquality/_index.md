---
title: GraphicsQualityOptions.CompositingQuality
linktitle: CompositingQuality
articleTitle: CompositingQuality
second_title: Aspose.Words für .NET
description: GraphicsQualityOptions CompositingQuality eigendom. Ruft die Renderqualität zusammengesetzter Bilder ab die für diese Grafik gezeichnet werden oder legt diese fest in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Ruft die Renderqualität zusammengesetzter Bilder ab, die für diese Grafik gezeichnet werden, oder legt diese fest.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

## Beispiele

Zeigt, wie Renderqualitätsoptionen beim Konvertieren von Dokumenten in Bildformate festgelegt werden.

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
