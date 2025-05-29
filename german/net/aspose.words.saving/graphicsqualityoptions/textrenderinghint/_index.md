---
title: GraphicsQualityOptions.TextRenderingHint
linktitle: TextRenderingHint
articleTitle: TextRenderingHint
second_title: Aspose.Words für .NET
description: Entdecken Sie die GraphicsQualityOptions TextRenderingHint-Eigenschaft für optimale Textdarstellung in Ihren Grafiken. Verbessern Sie noch heute die Bildqualität und Leistung!
type: docs
weight: 70
url: /de/net/aspose.words.saving/graphicsqualityoptions/textrenderinghint/
---
## GraphicsQualityOptions.TextRenderingHint property

Ruft den Renderingmodus für Text ab, der mit dieser Grafik verknüpft ist, oder legt diesen fest.

```csharp
public TextRenderingHint? TextRenderingHint { get; set; }
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
