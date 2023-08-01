---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words for .NET
description: Cell PreviousCell property. Gets the previous Cell node in C#.
type: docs
weight: 110
url: /net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Gets the previous [`Cell`](../) node.

```csharp
public Cell PreviousCell { get; }
```

## Remarks

The method can be used when you need to have typed access to cells of a [`Row`](../../row/). If a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) node is found in a row instead of a cell, it is automatically traversed to get a cell contained within.

## Examples

Shows how to enumerate through all table cells.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Enumerate through all cells of the table.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### See Also

* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
