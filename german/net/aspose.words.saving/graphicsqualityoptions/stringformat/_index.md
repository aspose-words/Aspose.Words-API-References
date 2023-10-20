---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: Aspose.Words für .NET
description: GraphicsQualityOptions StringFormat eigendom. Ruft Textlayoutinformationen z. B. Ausrichtung Ausrichtung und Tabstopps Anzeigemanipulationen z. B. Einfügen von Auslassungspunkten und nationale Ziffernersetzung und OpenTypeFunktionen ab oder legt diese fest in C#.
type: docs
weight: 60
url: /de/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Ruft Textlayoutinformationen (z. B. Ausrichtung, Ausrichtung und Tabstopps), Anzeigemanipulationen (z. B. Einfügen von Auslassungspunkten und nationale Ziffernersetzung) und OpenType-Funktionen ab oder legt diese fest.

```csharp
public StringFormat StringFormat { get; set; }
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
