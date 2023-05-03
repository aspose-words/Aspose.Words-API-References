---
title: Cell.ParentRow
linktitle: ParentRow
second_title: Aspose.Words for .NET API Reference
description: Cell ParentRow property. Returns the parent row of the cell in C#.
type: docs
weight: 90
url: /net/aspose.words.tables/cell/parentrow/
---
## ParentRow property

Returns the parent row of the cell.

```csharp
public Row ParentRow { get; }
```

## Remarks

Equivalent to FirstNonMarkupParentNode casted to [`Row`](../../row/).

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

* class [Row](../../row/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../cell/)
* assembly [Aspose.Words](../../../)
