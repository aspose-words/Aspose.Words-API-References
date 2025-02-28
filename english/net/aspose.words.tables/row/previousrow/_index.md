---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words for .NET
description: Access the PreviousRow property to easily retrieve the prior Row node, enhancing your data navigation and streamlining your coding workflow.
type: docs
weight: 100
url: /net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Gets the previous [`Row`](../) node.

```csharp
public Row PreviousRow { get; }
```

## Remarks

The method can be used when you need to have typed access to table rows. If a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) node is found in a table instead of a row, it is automatically traversed to get a row contained within.

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

* class [Row](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
