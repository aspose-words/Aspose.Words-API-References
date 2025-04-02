---
title: Cell.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for NodeJs
description: "Cell.tables property. Gets a collection of tables that are immediate children of the cell."
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Tables/cell/tables/
---

## Cell.tables property

Gets a collection of tables that are immediate children of the cell.


```js
get tables(): Aspose.Words.Tables.TableCollection
```

### Examples

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

* module [Aspose.Words.Tables](../../)
* class [Cell](../)

