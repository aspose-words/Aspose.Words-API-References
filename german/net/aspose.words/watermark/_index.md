---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Watermark, um Ihren Dokumenten einfach Wasserzeichen hinzuzufügen und anzupassen und so Professionalität und Markenimage zu verbessern.
type: docs
weight: 7520
url: /de/net/aspose.words/watermark/
---
## Watermark class

Stellt eine Klasse dar, die mit Dokumentwasserzeichen arbeitet.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Wasserzeichen](https://docs.aspose.com/words/net/working-with-watermark/) Dokumentationsartikel.

```csharp
public sealed class Watermark
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Ruft den Wasserzeichentyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Entfernt das Wasserzeichen. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Fügt dem Dokument ein Bildwasserzeichen hinzu. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Fügt dem Dokument ein Bildwasserzeichen hinzu. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Fügt dem Dokument ein Bildwasserzeichen hinzu. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Fügt dem Dokument ein Bildwasserzeichen hinzu. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Fügt dem Dokument ein Textwasserzeichen hinzu. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Fügt dem Dokument ein Textwasserzeichen hinzu. |

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
