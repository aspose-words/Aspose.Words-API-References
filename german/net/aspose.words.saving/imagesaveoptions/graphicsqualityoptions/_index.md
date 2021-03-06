---
title: GraphicsQualityOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht die Festlegung von Wiedergabemodus und -qualität für dieGraphics Objekt.
type: docs
weight: 20
url: /de/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Ermöglicht die Festlegung von Wiedergabemodus und -qualität für dieGraphics Objekt.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

### Bemerkungen

Verwenden Sie diese Eigenschaft, um die von der Aspose.Words-Engine standardmäßig bereitgestellten Grafikeinstellungen zu überschreiben.

Es wird nur wirksam, wenn ein Dokument in einem bildähnlichen Format gespeichert wird.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions)
* class [ImageSaveOptions](../../imagesaveoptions)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
