---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words für .NET
description: PdfSaveOptions ImageCompression eigendom. Gibt den Komprimierungstyp an der für alle Bilder im Dokument verwendet werden soll in C#.
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

BenutzenJpeg Mit dieser Funktion können Sie die Qualität der Bilder im Ausgabedokument steuern[`JpegQuality`](../jpegquality/) Eigentum.

BenutzenJpeg Bietet die schnellste Konvertierungsgeschwindigkeit im Vergleich zur Leistung anderer Komprimierungstypen, , aber in diesem Fall liegt eine verlustbehaftete JPEG-Komprimierung vor.

BenutzenAuto Ermöglicht die Steuerung der JPEG-Qualität im Ausgabedokument über[`JpegQuality`](../jpegquality/)Eigenschaft, , aber für andere Formate werden Rohpixeldaten mit Flate-Komprimierung extrahiert und gespeichert. Dieser Fall ist langsamer als die JPEG-Konvertierung, aber verlustfrei.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
