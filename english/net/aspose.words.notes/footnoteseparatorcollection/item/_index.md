---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: FootnoteSeparatorCollection Item property. Retrieves a FootnoteSeparator of the specified type in C#.
type: docs
weight: 20
url: /net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Retrieves a [`FootnoteSeparator`](../../footnoteseparator/) of the specified type.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Remarks

Returns `null` if the footnote/endnote separator of the specified type is not found.

## Examples

Shows how to manage footnote separator format.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Align footnote separator.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### See Also

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
