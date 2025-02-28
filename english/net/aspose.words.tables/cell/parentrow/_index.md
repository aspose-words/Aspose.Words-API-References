---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words for .NET
description: Discover the Cell ParentRow property to easily access the parent row of any cell, enhancing your data management and navigation efficiency.
type: docs
weight: 100
url: /net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Returns the parent row of the cell.

```csharp
public Row ParentRow { get; }
```

## Examples

Shows how to set a table to stay together on the same page.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### See Also

* class [Row](../../row/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
