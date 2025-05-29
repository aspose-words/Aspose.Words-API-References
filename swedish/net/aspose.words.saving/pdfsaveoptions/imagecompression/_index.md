---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words för .NET
description: Optimera din PDF med PdfSaveOptions ImageCompression-egenskap, så att du kan välja den bästa komprimeringstypen för livfulla bilder av hög kvalitet.
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

AnvändningJpeg låter dig kontrollera kvaliteten på bilderna i utdatadokumentet genom[`JpegQuality`](../jpegquality/) egendom.

AnvändningJpeg ger den snabbaste konverteringshastigheten jämfört med prestandan för andra komprimeringstyper, men i det här fallet finns det förlustbringande JPEG-komprimering.

AnvändningAuto låter oss kontrollera kvaliteten på JPEG i utdatadokumentet genom[`JpegQuality`](../jpegquality/)egenskap, men för andra format extraheras och sparas rå pixeldata med Flate-komprimering. Detta fall är långsammare än JPEG-konvertering men förlustfritt.

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

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Auto" för att använda
// "ImageCompression"-egenskapen för att kontrollera kvaliteten på JPEG-bilderna som hamnar i PDF-filen.
// Ställ in egenskapen "ImageCompression" till "PdfImageCompression.Jpeg" för att använda
// "ImageCompression"-egenskapen för att kontrollera kvaliteten på alla bilder som hamnar i PDF-filen.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Sätt egenskapen "JpegQuality" till "10" för att förstärka komprimeringen på bekostnad av bildkvaliteten.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Se även

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
