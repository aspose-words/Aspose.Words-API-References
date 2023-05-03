---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words for .NET API Reference
description: Paragraph IsInCell property. True if this paragraph is an immediate child of Cell false otherwise in C#.
type: docs
weight: 100
url: /net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

True if this paragraph is an immediate child of [`Cell`](../../../aspose.words.tables/cell/); false otherwise.

```csharp
public bool IsInCell { get; }
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

* class [Paragraph](../)
* namespace [Aspose.Words](../../paragraph/)
* assembly [Aspose.Words](../../../)
