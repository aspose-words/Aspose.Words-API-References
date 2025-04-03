---
title: TableCollection class
linktitle: TableCollection class
articleTitle: TableCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.TableCollection class. Provides typed access to a collection of [Table](../../aspose.words/table/) nodes"
type: docs
weight: 130
url: /nodejs-net/aspose.words.tables/tablecollection/
---

## TableCollection class

Provides typed access to a collection of [Table](../../aspose.words/table/) nodes.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




**Inheritance:** [TableCollection](./) → [NodeCollection](../../aspose.words/nodecollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
| [this[]](../../aspose.words/nodecollection/this[]/) | <br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../../aspose.words/nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ clear()](../../aspose.words/nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ contains(node)](../../aspose.words/nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ indexOf(node)](../../aspose.words/nodecollection/indexOf/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ insert(index, node)](../../aspose.words/nodecollection/insert/#number_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ remove(node)](../../aspose.words/nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ removeAt(index)](../../aspose.words/nodecollection/removeAt/#number) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ toArray()](./toArray/#default) | Copies all tables from the collection to a new array of tables. |

### Examples

Shows how to remove the first and last rows of all tables in a document.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let tables = doc.firstSection.body.tables.toArray();

expect(tables[0].rows.count).toEqual(5);
expect(tables[1].rows.count).toEqual(4);

for (var table of tables)
{
  table.firstRow?.remove();
  table.lastRow?.remove();
}

expect(tables[0].rows.count).toEqual(3);
expect(tables[1].rows.count).toEqual(2);
```

Shows how to find out if a tables are nested.

```js
test('CalculateDepthOfNestedTables', () => {
  let doc = new aw.Document(base.myDir + "Nested tables.docx");
  let tableNodes = doc.getChildNodes(aw.NodeType.Table, true);
  expect(tableNodes.count).toEqual(5);

  for (let i = 0; i < tableNodes.count; i++)
  {
    let table = tableNodes.at(i).asTable();

    // Find out if any cells in the table have other tables as children.
    let count = getChildTableCount(table);
    console.log("Table #{0} has {1} tables directly within its cells", i, count);

    // Find out if the table is nested inside another table, and, if so, at what depth.
    let tableDepth = getNestedDepthOfTable(table);

    if (tableDepth > 0)
      console.log("Table #{0} is nested inside another table at depth of {1}", i,
        tableDepth);
    else
      console.log("Table #{0} is a non nested table (is not a child of another table)", i);
  }
});


/// <summary>
/// Calculates what level a table is nested inside other tables.
/// </summary>
/// <returns>
/// An integer indicating the nesting depth of the table (number of parent table nodes).
/// </returns>
function getNestedDepthOfTable(table) {
  let depth = 0;
  let parent = table.getAncestor(aw.NodeType.Table);

  while (parent != null)
  {
    depth++;
    parent = parent.getAncestor(aw.NodeType.Table);
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
function getChildTableCount(table) {
  let childTableCount = 0;

  for (let row of table.rows.toArray())
  {
    for (let cell of row.cells.toArray())
    {
      if (cell.tables.count > 0)
        childTableCount++;
    }
  }

  return childTableCount;
}
```

### See Also

* module [Aspose.Words.Tables](../)
* class [NodeCollection](../../aspose.words/nodecollection/)

