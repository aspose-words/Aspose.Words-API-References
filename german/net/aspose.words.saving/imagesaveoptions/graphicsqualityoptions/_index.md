---
title: ImageSaveOptions.GraphicsQualityOptions
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ermöglicht die Angabe des RenderingModus und der Qualität fürGraphics Objekt.
type: docs
weight: 20
url: /de/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Ermöglicht die Angabe des Rendering-Modus und der Qualität fürGraphics Objekt.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

### Bemerkungen

Verwenden Sie diese Eigenschaft, um die von der Aspose.Words-Engine standardmäßig bereitgestellten Grafikeinstellungen zu überschreiben.

Es wird nur wirksam, wenn ein Dokument in einem bildähnlichen Format gespeichert wird.

### Beispiele

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


