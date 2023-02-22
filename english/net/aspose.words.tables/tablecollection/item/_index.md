---
title: Item
second_title: Aspose.Words for .NET API Reference
description: TableCollection property. Retrieves a Table at the given index in C#.
type: docs
weight: 10
url: /net/aspose.words.tables/tablecollection/item/
---
## TableCollection indexer

Retrieves a [`Table`](../../table/) at the given index.

```csharp
public Table this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // We can use the "ToArray" method on a row collection to clone it into an array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // We can use the "ToArray" method on a cell collection to clone it into an array.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### See Also

* class [Table](../../table/)
* class [TableCollection](../)
* namespace [Aspose.Words.Tables](../../tablecollection/)
* assembly [Aspose.Words](../../../)
