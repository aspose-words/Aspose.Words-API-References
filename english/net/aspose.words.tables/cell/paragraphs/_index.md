---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words for .NET
description: Discover the Cell Paragraphs property to access a collection of direct child paragraphs, enhancing your document's structure and readability.
type: docs
weight: 90
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
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.That(para.IsInCell, Is.True);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### See Also

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
