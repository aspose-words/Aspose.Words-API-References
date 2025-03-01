---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words for .NET
description: Discover the Row IsLastRow property, Easily identify if a row is the last in a table for streamlined data management and enhanced programming efficiency.
type: docs
weight: 50
url: /net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

True if this is the last row in a table; false otherwise.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
