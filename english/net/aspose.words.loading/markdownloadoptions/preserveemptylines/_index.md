---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words for .NET
description: MarkdownLoadOptions PreserveEmptyLines property. Gets or sets a boolean value indicating whether to preserve empty lines while load a Markdown document. The default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Gets or sets a boolean value indicating whether to preserve empty lines while load a Markdown document. The default value is `false`.

Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and end of the document are also ignored. This option allows to import such empty lines.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Examples

Shows how to preserve empty line while load a document.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### See Also

* class [MarkdownLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
