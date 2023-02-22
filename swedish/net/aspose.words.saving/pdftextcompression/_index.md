---
title: Enum PdfTextCompression
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfTextCompression uppräkning. Anger en typ av komprimering som tillämpas på allt innehåll i PDFfilen utom bilder.
type: docs
weight: 5250
url: /sv/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Anger en typ av komprimering som tillämpas på allt innehåll i PDF-filen utom bilder.

```csharp
public enum PdfTextCompression
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen komprimering. |
| Flate | `1` | Flate (ZIP) komprimering. |

### Exempel

Visar hur du använder textkomprimering när du sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "TextCompression" till "PdfTextCompression.None" för att inte tillämpa någon
// komprimering till text när vi sparar dokumentet till PDF.
// Ställ in egenskapen "TextCompression" till "PdfTextCompression.Flate" för att tillämpa ZIP-komprimering
// till text när vi sparar dokumentet till PDF. Ju större dokument, desto större inverkan kommer detta att ha.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


