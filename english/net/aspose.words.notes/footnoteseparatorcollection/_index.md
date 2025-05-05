---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Notes.FootnoteSeparatorCollection for easy access to footnote separators in your documents. Enhance your document formatting today!
type: docs
weight: 5000
url: /net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Provides typed access to [`FootnoteSeparator`](../footnoteseparator/) nodes of a document.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Constructors

| Name | Description |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Retrieves a [`FootnoteSeparator`](../footnoteseparator/) of the specified type. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Examples

Shows how to manage footnote separator format.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Align footnote separator.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### See Also

* class [FootnoteSeparator](../footnoteseparator/)
* namespace [Aspose.Words.Notes](../../aspose.words.notes/)
* assembly [Aspose.Words](../../)
