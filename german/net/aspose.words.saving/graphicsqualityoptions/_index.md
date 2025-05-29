---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.GraphicsQualityOptions, um die Grafikqualität von Dokumenten mit anpassbaren Optionen für eine hervorragende Ausgabe zu verbessern.
type: docs
weight: 5790
url: /de/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Ermöglicht die Angabe zusätzlicherGraphics Qualitätsoptionen.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

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
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie zusammengesetzte Bilder in diese Grafik gezeichnet werden. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Ruft die Rendering-Qualität von zusammengesetzten Bildern ab, die in diese Grafik gezeichnet werden, oder legt diese fest. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Ruft den mit dieser Grafik verknüpften Interpolationsmodus ab oder legt ihn fest. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Ruft die Rendering-Qualität für diese Grafik ab oder legt sie fest. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Ruft Textlayoutinformationen (wie Ausrichtung, Orientierung und Tabstopps), Anzeigemanipulationen (wie Auslassungspunkte und nationale Ziffernersetzung) und OpenType-Funktionen ab oder legt diese fest. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Ruft den Renderingmodus für Text ab, der mit dieser Grafik verknüpft ist, oder legt diesen fest. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob WrapMode TileFlipXY ist. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
