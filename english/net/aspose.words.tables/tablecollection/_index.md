---
title: TableCollection Class
linktitle: TableCollection
articleTitle: TableCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.TableCollection class. Provides typed access to a collection of Table nodes in C#.
type: docs
weight: 6630
url: /net/aspose.words.tables/tablecollection/
---
## TableCollection class

Provides typed access to a collection of [`Table`](../table/) nodes.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public class TableCollection : NodeCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Gets the number of nodes in the collection. |
| [Item](../../aspose.words.tables/tablecollection/item/) { get; } | Retrieves a [`Table`](../table/) at the given index. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Provides a simple "foreach" style iteration over the collection of nodes. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words.tables/tablecollection/toarray/#toarray_1)() | Copies all tables from the collection to a new array of tables. (2 methods) |

## Examples

Shows how to remove the first and last rows of all tables in a document.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

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

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
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

* class [NodeCollection](../../aspose.words/nodecollection/)
* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
