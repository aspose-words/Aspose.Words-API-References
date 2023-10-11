---
title: GraphicsQualityOptions.StringFormat
second_title: Aspose.Words für .NET-API-Referenz
description: GraphicsQualityOptions eigendom. Ruft Textlayoutinformationen z. B. Ausrichtung Ausrichtung und Tabstopps Anzeigemanipulationen z. B. Einfügen von Auslassungspunkten und nationale Ziffernersetzung und OpenTypeFunktionen ab oder legt diese fest.
type: docs
weight: 60
url: /de/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Ruft Textlayoutinformationen (z. B. Ausrichtung, Ausrichtung und Tabstopps), Anzeigemanipulationen (z. B. Einfügen von Auslassungspunkten und nationale Ziffernersetzung) und OpenType-Funktionen ab oder legt diese fest.

```csharp
public StringFormat StringFormat { get; set; }
```

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

* class [GraphicsQualityOptions](../)
* namensraum [Aspose.Words.Saving](../../graphicsqualityoptions/)
* Montage [Aspose.Words](../../../)


