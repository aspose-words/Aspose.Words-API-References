---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words för .NET
description: PdfSaveOptions JpegQuality fast egendom. Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEGbilderna i PDFdokumentet i C#.
type: docs
weight: 220
url: /sv/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEG-bilderna i PDF-dokumentet.

```csharp
public int JpegQuality { get; set; }
```

## Anmärkningar

Standardvärdet är 100.

Denna egenskap används i samband med[`ImageCompression`](../imagecompression/) alternativ.

Har endast effekt när ett dokument innehåller JPEG-bilder.

Använd den här egenskapen för att hämta eller ställa in kvaliteten på bilderna i ett dokument när du sparar i PDF-format. Värdet kan variera från 0 till 100 där 0 betyder sämsta kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minsta komprimering. Om kvalitet är 100 och källbilden är JPEG, betyder det ingen komprimering - originalbytes kommer att sparas.

## Exempel

Visar hur man anger en komprimeringstyp för alla bilder i ett dokument som vi konverterar till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Auto" för att använda
// Egenskapen "ImageCompression" för att kontrollera kvaliteten på Jpeg-bilderna som hamnar i utdata-PDF.
// Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Jpeg" för att använda
// Egenskapen "ImageCompression" för att kontrollera kvaliteten på alla bilder som hamnar i utdata-PDF.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Ställ in egenskapen "JpegQuality" till "10" för att stärka komprimeringen till priset av bildkvalitet.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
