---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Grafiken mit der Eigenschaft „ImageSaveOptions GraphicsQualityOptions“, die präzise Rendering-Modi und überragende Qualität für atemberaubende visuelle Darstellungen ermöglicht.
type: docs
weight: 20
url: /de/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Ermöglicht die Angabe von Rendering-Modus und Qualität für dieGraphics Objekt.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Bemerkungen

Verwenden Sie diese Eigenschaft, um die standardmäßig von der Aspose.Words-Engine bereitgestellten Grafikeinstellungen zu überschreiben.

Es wird nur wirksam, wenn ein Dokument in einem bildähnlichen Format gespeichert wird.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
