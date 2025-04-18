---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words for .NET
description: Discover the FootnoteOptions Columns property to easily format your footnotes with customizable column layouts for enhanced readability and presentation.
type: docs
weight: 10
url: /net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Specifies the number of columns with which the footnotes area is formatted.

```csharp
public int Columns { get; set; }
```

## Remarks

If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

## Examples

Shows how to split the footnote section into a given number of columns.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### See Also

* class [FootnoteOptions](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
