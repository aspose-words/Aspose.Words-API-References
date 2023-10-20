---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words für .NET
description: PdfSaveOptions JpegQuality eigendom. Ruft einen Wert ab oder legt diesen fest der die Qualität der JPEGBilder im PDFDokument bestimmt in C#.
type: docs
weight: 220
url: /de/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt diesen fest, der die Qualität der JPEG-Bilder im PDF-Dokument bestimmt.

```csharp
public int JpegQuality { get; set; }
```

## Bemerkungen

Der Standardwert ist 100.

Diese Eigenschaft wird in Verbindung mit verwendet[`ImageCompression`](../imagecompression/) Möglichkeit.

Hat nur Auswirkungen, wenn ein Dokument JPEG-Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im PDF-Format abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 schlechteste Qualität, aber maximale Komprimierung und 100 beste Qualität, aber minimale Komprimierung bedeutet. Wenn Qualität 100 ist und das Quellbild JPEG ist, bedeutet dies, dass keine Komprimierung erfolgt – die ursprünglichen Bytes werden gespeichert.

## Beispiele

Zeigt, wie man einen Komprimierungstyp für alle Bilder in einem Dokument angibt, das wir in PDF konvertieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „ImageCompression“ auf „PdfImageCompression.Auto“, um die zu verwenden
// „ImageCompression“-Eigenschaft zur Steuerung der Qualität der JPEG-Bilder, die im Ausgabe-PDF landen.
// Setzen Sie die Eigenschaft „ImageCompression“ auf „PdfImageCompression.Jpeg“, um die zu verwenden
// „ImageCompression“-Eigenschaft zur Steuerung der Qualität aller Bilder, die im Ausgabe-PDF landen.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Setzen Sie die Eigenschaft „JpegQuality“ auf „10“, um die Komprimierung auf Kosten der Bildqualität zu verstärken.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
