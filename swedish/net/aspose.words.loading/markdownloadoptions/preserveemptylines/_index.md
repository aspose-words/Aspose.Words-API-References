---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PreserveEmptyLines i MarkdownLoadOptions förbättrar inläsningen av ditt Markdown-dokument genom att bevara tomma rader för förbättrad läsbarhet.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Hämtar eller ställer in ett booleskt värde som anger om tomma rader ska behållas vid laddning av enMarkdown dokument. Standardvärdet är`falsk` .

Normalt ignoreras tomma rader mellan blocknivåelement i Markdown. Tomma rader i början och slutet av dokumentet ignoreras också. Det här alternativet tillåter import av sådana tomma rader.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Exempel

Visar hur man bevarar tomma rader när man laddar ett dokument.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Se även

* class [MarkdownLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
