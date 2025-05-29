---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions TextCompression för att optimera dina dokument. Välj den bästa komprimeringstypen för effektiv textlagring och snabbare inläsning.
type: docs
weight: 310
url: /sv/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Anger komprimeringstyp som ska användas för allt textinnehåll i dokumentet.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Anmärkningar

Standard ärFlate.

Ökar utskriftsstorleken avsevärt när ett dokument sparas utan komprimering.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
