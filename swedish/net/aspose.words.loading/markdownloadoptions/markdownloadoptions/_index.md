---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck MarkdownLoadOptions-konstruktorn för att enkelt initiera MarkdownLoadOptions-instanser för förbättrad dokumentbehandling och anpassning.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Initierar en ny instans av[`MarkdownLoadOptions`](../) klass.

```csharp
public MarkdownLoadOptions()
```

## Anmärkningar

Ställs in automatiskt[`LoadFormat`](../../../aspose.words/loadformat/) tillMarkdown .

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
