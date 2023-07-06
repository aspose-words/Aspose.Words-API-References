---
title: Cell.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words for .NET
description: Cell Tables property. Gets a collection of tables that are immediate children of the cell in C#.
type: docs
weight: 120
url: /net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

Gets a collection of tables that are immediate children of the cell.

```csharp
public TableCollection Tables { get; }
```

## Examples

Shows how to find out if a tables are nested.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Find out if any cells in the table have other tables as children.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Find out if the table is nested inside another table, and, if so, at what depth.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calculates what level a table is nested inside other tables.
/// </summary>
/// <returns>
/// An integer indicating the nesting depth of the table (number of parent table nodes).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// Determines if a table contains any immediate child table within its cells.
/// Do not recursively traverse through those tables to check for further tables.
/// </summary>
/// <returns>
/// Returns true if at least one child cell contains a table.
/// Returns false if no cells in the table contain a table.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### See Also

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
