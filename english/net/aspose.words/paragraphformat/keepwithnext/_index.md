---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words for .NET API Reference
description: ParagraphFormat KeepWithNext property. True if the paragraph is to remains on the same page as the paragraph that follows it in C#.
type: docs
weight: 160
url: /net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

True if the paragraph is to remains on the same page as the paragraph that follows it.

```csharp
public bool KeepWithNext { get; set; }
```

## Examples

Shows how to set a table to stay together on the same page.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../paragraphformat/)
* assembly [Aspose.Words](../../../)
