---
title: GraphicsQualityOptions.SmoothingMode
linktitle: SmoothingMode
articleTitle: SmoothingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die SmoothingMode-Eigenschaft von GraphicsQualityOptions, um Ihre Rendering-Qualität zu verbessern und Ihre Grafikleistung mühelos zu steigern.
type: docs
weight: 50
url: /de/net/aspose.words.saving/graphicsqualityoptions/smoothingmode/
---
## GraphicsQualityOptions.SmoothingMode property

Ruft die Rendering-Qualität für diese Grafik ab oder legt sie fest.

```csharp
public SmoothingMode? SmoothingMode { get; set; }
```

## Beispiele

Zeigt, wie Sie beim Konvertieren von Dokumenten in Bildformate Optionen für die Renderqualität festlegen.

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
