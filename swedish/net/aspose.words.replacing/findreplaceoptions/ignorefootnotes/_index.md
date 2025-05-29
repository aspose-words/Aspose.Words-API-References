---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreFootnotes för att enkelt hantera fotnoter i dina dokument. Förbättra redigeringseffektiviteten med den här enkla växlingsknappen!
type: docs
weight: 90
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Hämtar eller ställer in ett booleskt värde som anger att fotnoter ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Exempel

Visar hur man ignorerar fotnoter under en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Sätt flaggan "IgnoreFootnotes" till "sant" för att få sök-och-ersätt-funktionen
// operation för att ignorera text i fotnoter.
// Sätt flaggan "IgnoreFootnotes" till "false" för att få sök-och-ersätt-funktionen
// operation för att även söka efter text inuti fotnoter.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
