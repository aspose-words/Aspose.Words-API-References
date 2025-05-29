---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfTextCompression enum för effektiv PDF-komprimering, vilket förbättrar filstorlek och prestanda samtidigt som kvaliteten bibehålls.
type: docs
weight: 6330
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
| Flate | `1` | Platt (ZIP) komprimering. |

## Exempel

Visar hur man tillämpar textkomprimering när man sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "TextCompression" till "PdfTextCompression.None" för att inte tillämpa några
// komprimering till text när vi sparar dokumentet som PDF.
// Ställ in egenskapen "TextCompression" till "PdfTextCompression.Flate" för att tillämpa ZIP-komprimering
// till text när vi sparar dokumentet som PDF. Ju större dokumentet är, desto större effekt får detta.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
