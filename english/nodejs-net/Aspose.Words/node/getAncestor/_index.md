---
title: Node.getAncestor method
linktitle: getAncestor method
articleTitle: getAncestor method
second_title: Aspose.Words for NodeJs
description: "Node.getAncestor method. Gets the first ancestor of the specified [NodeType](../../nodetype/)."
type: docs
weight: 440
url: /nodejs-net/Aspose.Words/node/getAncestor/
---

## getAncestor(ancestorType) {#nodetype}

Gets the first ancestor of the specified [NodeType](../../nodetype/).



```js
getAncestor(ancestorType: Aspose.Words.NodeType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | [NodeType](../../nodetype/) | The node type of the ancestor to retrieve. |

### Returns

The ancestor of the specified type or ``null`` if no ancestor of this type was found.


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

* module [Aspose.Words](../../)
* class [Node](../)

