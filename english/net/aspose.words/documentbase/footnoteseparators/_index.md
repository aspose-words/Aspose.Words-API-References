---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words for .NET
description: Access and customize footnote and endnote separators in your document with DocumentBase's FootnoteSeparators property for enhanced formatting control.
type: docs
weight: 40
url: /net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Provides access to the footnote/endnote separators defined in the document.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## Examples

Shows how to remove endnote separator.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Remove endnote separator.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Shows how to manage footnote separator format.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Align footnote separator.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### See Also

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
