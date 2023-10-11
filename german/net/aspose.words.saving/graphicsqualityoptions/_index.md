---
title: Class GraphicsQualityOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.GraphicsQualityOptions klas. Ermöglicht die Angabe zusätzlicherGraphics Qualitätsoptionen.
type: docs
weight: 5040
url: /de/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Ermöglicht die Angabe zusätzlicherGraphics Qualitätsoptionen.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class GraphicsQualityOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, wie zusammengesetzte Bilder in diese Grafik gezeichnet werden. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Ruft die Renderqualität zusammengesetzter Bilder ab, die für diese Grafik gezeichnet werden, oder legt diese fest. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Ruft den dieser Grafik zugeordneten Interpolationsmodus ab oder legt diesen fest. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Ruft die Renderqualität für diese Grafik ab oder legt sie fest. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Ruft Textlayoutinformationen (z. B. Ausrichtung, Ausrichtung und Tabstopps), Anzeigemanipulationen (z. B. Einfügen von Auslassungspunkten und nationale Ziffernersetzung) und OpenType-Funktionen ab oder legt diese fest. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Ruft den Rendering-Modus für Text ab, der dieser Grafik zugeordnet ist, oder legt diesen fest. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob WrapMode TileFlipXY ist. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


