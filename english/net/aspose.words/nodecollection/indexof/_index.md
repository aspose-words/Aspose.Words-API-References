---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words for .NET
description: Discover the NodeCollection IndexOf method to efficiently find the zero-based index of any specified node in your collections.
type: docs
weight: 70
url: /net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Returns the zero-based index of the specified node.

```csharp
public int IndexOf(Node node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | Node | The node to locate. |

### Return Value

The zero-based index of the node within the collection, if found; otherwise, -1.

## Remarks

This method performs a linear search; therefore, the average execution time is proportional to [`Count`](../count/).

## Examples

Shows how to get the index of a node in a collection.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.That(allTables.IndexOf(table), Is.EqualTo(0));

Row row = table.Rows[2];

Assert.That(table.IndexOf(row), Is.EqualTo(2));

Cell cell = row.LastCell;

Assert.That(row.IndexOf(cell), Is.EqualTo(4));
```

### See Also

* class [Node](../../node/)
* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
