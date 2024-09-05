---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words for .NET
description: MarkdownLoadOptions ImportUnderlineFormatting property. Gets or sets a boolean value indicating either to recognize a sequence of two plus characters  as underline text formatting. The default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Gets or sets a boolean value indicating either to recognize a sequence of two plus characters "++" as underline text formatting. The default value is `false`.

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Examples

Shows how to recognize plus characters "++" as underline text formatting.

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

### See Also

* class [MarkdownLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
