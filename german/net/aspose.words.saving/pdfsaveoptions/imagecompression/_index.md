---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre PDF-Datei mit der ImageCompression-Eigenschaft von PdfSaveOptions und wählen Sie so den besten Komprimierungstyp für lebendige, qualitativ hochwertige Bilder aus.
type: docs
weight: 200
url: /de/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Gibt den Komprimierungstyp an, der für alle Bilder im Dokument verwendet werden soll.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Bemerkungen

Standard istAuto.

VerwendenJpeg ermöglicht Ihnen die Kontrolle der Bildqualität im Ausgabedokument über die[`JpegQuality`](../jpegquality/) Eigentum.

VerwendenJpeg bietet im Vergleich zur Leistung anderer Komprimierungstypen die schnellste Konvertierungsgeschwindigkeit, , in diesem Fall handelt es sich jedoch um eine verlustbehaftete JPEG-Komprimierung.

VerwendenAuto ermöglicht die Kontrolle der JPEG-Qualität im Ausgabedokument durch die[`JpegQuality`](../jpegquality/)Eigenschaft, , aber für andere Formate werden Rohpixeldaten extrahiert und mit Flate-Komprimierung gespeichert. Dieser Fall ist langsamer als die JPEG-Konvertierung, aber verlustfrei.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
