---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImportFormatOptions AdjustSentenceAndWordSpacing. Styr enkelt automatiskt menings- och ordavstånd för förbättrad texttydlighet.
type: docs
weight: 20
url: /sv/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Hämtar eller ställer in ett booleskt värde som anger om avståndet mellan meningar och ord ska justeras automatiskt. Standardvärdet är`falsk` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Exempel

Visar hur man justerar avståndet mellan meningar och ord automatiskt.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
