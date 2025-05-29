---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die StringFormat-Eigenschaft „GraphicsQualityOptions“ für eine verbesserte Textlayoutsteuerung, einschließlich Ausrichtung, Auslassungspunkten und OpenType-Funktionen für eine bessere Anzeige.
type: docs
weight: 60
url: /de/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Ruft Textlayoutinformationen (wie Ausrichtung, Orientierung und Tabstopps), Anzeigemanipulationen (wie Auslassungspunkte und nationale Ziffernersetzung) und OpenType-Funktionen ab oder legt diese fest.

```csharp
public StringFormat StringFormat { get; set; }
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
