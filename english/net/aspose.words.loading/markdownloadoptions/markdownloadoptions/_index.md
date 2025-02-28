---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words for .NET
description: Discover the MarkdownLoadOptions constructor to easily initialize MarkdownLoadOptions instances for enhanced document processing and customization.
type: docs
weight: 10
url: /net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Initializes a new instance of [`MarkdownLoadOptions`](../) class.

```csharp
public MarkdownLoadOptions()
```

## Remarks

Automatically sets [`LoadFormat`](../../../aspose.words/loadformat/) to Markdown.

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
