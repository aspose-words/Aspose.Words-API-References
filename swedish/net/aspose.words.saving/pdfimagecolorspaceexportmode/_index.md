---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words PdfImageColorSpaceExportMode-enum för att optimera bildfärgsvalet i dina PDF-dokument för fantastiska bilder.
type: docs
weight: 6270
url: /sv/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Anger hur färgrymden ska väljas för bilderna i PDF-dokumentet.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Aspose.Words väljer automatiskt det lämpligaste färgutrymmet för varje bild. |
| SimpleCmyk | `1` | Aspose.Words omvandlar RGB-bilder till CMYK-färgrymd med hjälp av en enkel formel. |

## Exempel

Visar hur man ställer in ett annat färgutrymme för bilder i ett dokument när vi exporterar det till PDF.

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

// Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.Auto" för att få Aspose.Words till
// väljer automatiskt färgrymden för bilder i dokumentet som konverteras till PDF.
// I de flesta fall kommer färgrymden att vara RGB.
// Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.SimpleCmyk"
// för att använda CMYK-färgrymden för alla bilder i den sparade PDF-filen.
// Aspose.Words kommer också att tillämpa Flate-komprimering på alla bilder och ignorera värdet på egenskapen "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
