---
title: Paragraphs
second_title: Aspose.Words for .NET API Reference
description: Cell property. Gets a collection of paragraphs that are immediate children of the cell in C#.
type: docs
weight: 80
url: /net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Gets a collection of paragraphs that are immediate children of the cell.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../cell/)
* assembly [Aspose.Words](../../../)
