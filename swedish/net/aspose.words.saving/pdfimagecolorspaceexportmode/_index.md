---
title: Enum PdfImageColorSpaceExportMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode uppräkning. Anger hur färgrymden kommer att väljas för bilderna i PDFdokument.
type: docs
weight: 5200
url: /sv/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Anger hur färgrymden kommer att väljas för bilderna i PDF-dokument.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Aspose.Words väljer automatiskt den lämpligaste färgrymden för varje bild. |
| SimpleCmyk | `1` | Aspose.Words döljer RGB-bilder till CMYK-färgrymd med en enkel formel. |

### Exempel

Visar hur du ställer in en annan färgrymd för bilder i ett dokument när vi exporterar det till PDF.

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

// Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.Auto" för att få Aspose.Words till
// väljer automatiskt färgrymden för bilder i dokumentet som det konverterar till PDF.
// I de flesta fall kommer färgrymden att vara RGB.
// Ställ in egenskapen "ImageColorSpaceExportMode" till "PdfImageColorSpaceExportMode.SimpleCmyk"
// för att använda CMYK-färgrymden för alla bilder i den sparade PDF-filen.
// Aspose.Words kommer också att tillämpa Flate-komprimering på alla bilder och ignorerar "ImageCompression"-egenskapens värde.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


