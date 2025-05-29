---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.TextWatermarkOptions für anpassbare Textwasserzeichen. Werten Sie Ihre Dokumente mit einzigartigen, professionellen Branding-Optionen auf!
type: docs
weight: 7290
url: /de/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Text angegeben werden können.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Wasserzeichen](https://docs.aspose.com/words/net/working-with-watermark/) Dokumentationsartikel.

```csharp
public class TextWatermarkOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Ruft die Schriftfarbe ab oder legt sie fest. Der Standardwert istSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Ruft den Namen der Schriftfamilie ab oder legt ihn fest. Der Standardwert ist "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Ruft die Schriftgröße ab oder legt sie fest. Der Standardwert ist 0 (auto). |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der für die Deckkraft des Wasserzeichens verantwortlich ist. Der Standardwert ist`WAHR` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Ruft das Layout des Wasserzeichens ab oder legt es fest. Der Standardwert istDiagonal . |

## Beispiele

Zeigt, wie ein Textwasserzeichen erstellt wird.

```csharp
Document doc = new Document();

// Fügen Sie ein Wasserzeichen im Klartext hinzu.
doc.Watermark.SetText("Aspose Watermark");

// Wenn wir die Textformatierung bearbeiten und sie als Wasserzeichen verwenden möchten,
// Dies können wir tun, indem wir beim Erstellen des Wasserzeichens ein TextWatermarkOptions-Objekt übergeben.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Wir können ein Wasserzeichen aus einem Dokument wie diesem entfernen.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
