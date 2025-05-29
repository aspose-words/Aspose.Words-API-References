---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre PDF-Bilder mit der JpegQuality-Eigenschaft von PdfSaveOptions, mit der Sie die JPEG-Qualität für beeindruckende Dokumentvisualisierungen steuern können.
type: docs
weight: 220
url: /de/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder im PDF-Dokument bestimmt.

```csharp
public int JpegQuality { get; set; }
```

## Bemerkungen

Der Standardwert ist 100.

Diese Eigenschaft wird in Verbindung mit dem[`ImageCompression`](../imagecompression/) Option.

Hat nur Auswirkungen, wenn ein Dokument JPEG-Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im PDF-Format abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 die schlechteste Qualität, aber maximale Komprimierung und 100 die beste Qualität, aber minimale Komprimierung bedeutet. Wenn die Qualität 100 beträgt und das Quellbild JPEG ist, bedeutet dies keine Komprimierung – die Originalbytes werden gespeichert.

## Beispiele

Zeigt, wie ein Komprimierungstyp für alle Bilder in einem Dokument angegeben wird, das wir in PDF konvertieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// Setzen Sie die Eigenschaft „ImageCompression“ auf „PdfImageCompression.Auto“, um die
// Eigenschaft „ImageCompression“ zur Steuerung der Qualität der JPEG-Bilder, die im Ausgabe-PDF landen.
// Setzen Sie die Eigenschaft „ImageCompression“ auf „PdfImageCompression.Jpeg“, um die
// Eigenschaft „ImageCompression“ zur Steuerung der Qualität aller Bilder, die im Ausgabe-PDF landen.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Setzen Sie die Eigenschaft „JpegQuality“ auf „10“, um die Komprimierung auf Kosten der Bildqualität zu verstärken.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
