---
title: MarkdownLoadOptions.SoftLineBreakCharacter
linktitle: SoftLineBreakCharacter
articleTitle: SoftLineBreakCharacter
second_title: Aspose.Words for .NET
description: Set custom soft line break characters in Markdown documents for better formatting with this flexible load option.
type: docs
weight: 40
url: /net/aspose.words.loading/markdownloadoptions/softlinebreakcharacter/
---
## MarkdownLoadOptions.SoftLineBreakCharacter property

Gets or sets a character value representing `soft line break`. The default value is `SPACE (U+0020)`.

```csharp
public char SoftLineBreakCharacter { get; set; }
```

## Remarks

Note, setting this option to [`LineBreakChar`](../../../aspose.words/controlchar/linebreakchar/) allows you to load soft line breaks as hard line breaks.

## Examples

Shows how to set soft line break character.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes("line1\nline2")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
    loadOptions.SoftLineBreakCharacter = ControlChar.LineBreakChar;
    Document doc = new Document(stream, loadOptions);

    Assert.That(doc.GetText().Trim(), Is.EqualTo("line1\u000bline2"));
}
```

### See Also

* class [MarkdownLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
