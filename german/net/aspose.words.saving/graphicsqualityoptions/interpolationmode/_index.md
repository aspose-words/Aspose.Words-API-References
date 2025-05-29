---
title: GraphicsQualityOptions.InterpolationMode
linktitle: InterpolationMode
articleTitle: InterpolationMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die InterpolationMode-Eigenschaft von GraphicsQualityOptions, um die Interpolationseinstellungen Ihrer Grafiken für eine verbesserte visuelle Qualität einfach anzupassen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Ruft den mit dieser Grafik verknüpften Interpolationsmodus ab oder legt ihn fest.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
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
