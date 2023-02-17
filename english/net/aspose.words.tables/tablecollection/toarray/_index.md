---
title: TableCollection.ToArray
second_title: Aspose.Words for .NET API Reference
description: TableCollection method. Copies all tables from the collection to a new array of tables in C#.
type: docs
weight: 20
url: /net/aspose.words.tables/tablecollection/toarray/
---
## TableCollection.ToArray method

Copies all tables from the collection to a new array of tables.

```csharp
public Table[] ToArray()
```

### Return Value

An array of tables.

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
