---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words för .NET
description: PdfSaveOptions ImageCompression fast egendom. Anger komprimeringstyp som ska användas för alla bilder i dokumentet i C#.
type: docs
weight: 200
url: /sv/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Anger komprimeringstyp som ska användas för alla bilder i dokumentet.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Anmärkningar

Standard ärAuto.

Använder sig avJpeg låter dig kontrollera kvaliteten på bilderna i det utgående dokumentet genom[`JpegQuality`](../jpegquality/) fast egendom.

Använder sig avJpeg ger den snabbaste omvandlingshastigheten jämfört med prestanda för andra komprimeringstyper, men i det här fallet finns det förlust av JPEG-komprimering.

Använder sig avAuto låter dig kontrollera kvaliteten på Jpeg i utdatadokumentet genom[`JpegQuality`](../jpegquality/)property, men för andra format extraheras rå pixeldata och sparas med Flate-komprimering. Det här fallet är långsammare än Jpeg-konvertering men förlustfritt.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
