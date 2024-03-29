---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words för .NET
description: PdfSaveOptions ExportLanguageToSpanTag fast egendom. Hämtar eller ställer in ett värde som avgör om en Spantagg ska skapas eller inte i dokumentstrukturen för att exportera textspråket i C#.
type: docs
weight: 150
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Hämtar eller ställer in ett värde som avgör om en "Span"-tagg ska skapas eller inte i dokumentstrukturen för att exportera textspråket.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`och "Lang"-attribut är kopplat till en markerad innehållssekvens i en sidinnehållsström.

När värdet är`Sann` "Span"-taggen skapas för texten med icke-standardspråk och "Lang"-attribut är kopplat till denna tagg.

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
