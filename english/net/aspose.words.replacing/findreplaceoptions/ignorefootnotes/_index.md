---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words for .NET
description: FindReplaceOptions IgnoreFootnotes property. Gets or sets a boolean value indicating either to ignore footnotes. The default value is false in C#.
type: docs
weight: 90
url: /net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Gets or sets a boolean value indicating either to ignore footnotes. The default value is `false`.

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Examples

Shows how to ignore footnotes during a find-and-replace operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
// operation to ignore text inside footnotes.
// Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
// operation to also search for text inside footnotes.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
