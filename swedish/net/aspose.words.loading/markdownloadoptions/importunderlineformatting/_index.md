---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImportUnderlineFormatting i MarkdownLoadOptions. Kontrollera formateringen av understruken text med en enkel boolesk inställning. Förbättra din Markdown-upplevelse!
type: docs
weight: 20
url: /sv/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Hämtar eller ställer in ett booleskt värde som anger att en sekvens av två plustecken "++" ska kännas igen som understruken textformatering. Standardvärdet är`falsk` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Exempel

Visar hur man känner igen plustecknen "++" som understruken textformatering.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Se även

* class [MarkdownLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
