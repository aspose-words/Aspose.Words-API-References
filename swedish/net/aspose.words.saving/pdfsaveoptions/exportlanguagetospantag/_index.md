---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions egenskap ExportLanguageToSpanTag. Styr export av textspråk med Span-taggar för förbättrad dokumentstruktur och tillgänglighet.
type: docs
weight: 150
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Hämtar eller anger ett värde som avgör om en "Span"-tagg ska skapas i dokumentstrukturen för att exportera textspråket.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`och attributet "Lang" är kopplat till en sekvens av markerat innehåll i en sidinnehållsström.

När värdet är`sann` Taggen "Span" skapas för texten med ett icke-standardspråk, `language `, och attributet "Lang" är kopplat till taggen.

Detta värde ignoreras när[`ExportDocumentStructure`](../exportdocumentstructure/) är`falsk` .

## Exempel

Visar hur man skapar en "Span"-tagg i dokumentstrukturen för att exportera textspråket.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Observera att när "ExportDocumentStructure" är falskt ignoreras "ExportLanguageToSpanTag".
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
