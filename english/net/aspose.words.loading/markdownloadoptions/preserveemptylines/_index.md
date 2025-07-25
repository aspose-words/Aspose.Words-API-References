---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words for .NET
description: Discover how the MarkdownLoadOptions PreserveEmptyLines property enhances your Markdown document loading by preserving empty lines for improved readability.
type: docs
weight: 30
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

    Assert.That(doc.GetText(), Is.EqualTo("\rLine1\r\rLine2\r\f"));
}
```

### See Also

* class [MarkdownLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
