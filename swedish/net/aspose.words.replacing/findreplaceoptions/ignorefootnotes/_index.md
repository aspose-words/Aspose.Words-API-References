---
title: FindReplaceOptions.IgnoreFootnotes
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar att antingen ignorera fotnoter. Standardvärdet ärfalsk .
type: docs
weight: 90
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Hämtar eller ställer in ett booleskt värde som indikerar att antingen ignorera fotnoter. Standardvärdet är`falsk` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

### Exempel

Visar hur man ignorerar fotnoter under en sök-och-ersätt-operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Ställ in "Ignorera fotnoter"-flaggan till "true" för att få sök-och-ersätt
// operation för att ignorera text i fotnoter.
// Sätt flaggan "Ignorera fotnoter" till "false" för att få sök-och-ersätt
// operation för att även söka efter text i fotnoter.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


