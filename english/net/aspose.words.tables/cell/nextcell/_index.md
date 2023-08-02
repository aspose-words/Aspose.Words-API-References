---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words for .NET
description: Cell NextCell property. Gets the next Cell node in C#.
type: docs
weight: 70
url: /net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Gets the next [`Cell`](../) node.

```csharp
public Cell NextCell { get; }
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
