---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.FootnoteSeparatorType enum to customize footnote and endnote separators, enhancing document formatting and readability.
type: docs
weight: 5030
url: /net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Specifies the type of the footnote/endnote separator.

```csharp
public enum FootnoteSeparatorType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FootnoteSeparator | `0` | Separator between main text and footnote text. |
| FootnoteContinuationSeparator | `1` | Printed above footnote text on a page when the text must be continued from a previous page. |
| FootnoteContinuationNotice | `2` | Printed below footnote text on a page when footnote text must be continued on a succeeding page. |
| EndnoteSeparator | `3` | Separator between main text and endnote text. |
| EndnoteContinuationSeparator | `4` | Printed above endnote text on a page when the text must be continued from a previous page. |
| EndnoteContinuationNotice | `5` | Printed below endnote text on a page when endnote text must be continued on a succeeding page. |

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

* namespace [Aspose.Words.Notes](../../aspose.words.notes/)
* assembly [Aspose.Words](../../)
