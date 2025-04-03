---
title: Table.nodeType property
linktitle: nodeType property
articleTitle: nodeType property
second_title: Aspose.Words for NodeJs
description: "Table.nodeType property. Returns [NodeType.Table](../../nodetype/#Table)."
type: docs
weight: 210
url: /nodejs-net/aspose.words/table/nodeType/
---

## Table.nodeType property

Returns [NodeType.Table](../../nodetype/#Table).



```js
get nodeType(): Aspose.Words.NodeType
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

Shows how to traverse a composite node's tree of child nodes.

```js
test('RecurseChildren', () => {
  let doc = new aw.Document(base.myDir + "Paragraphs.docx");

  // Any node that can contain child nodes, such as the document itself, is composite.
  expect(doc.isComposite).toEqual(true);

  // Invoke the recursive function that will go through and print all the child nodes of a composite node.
  traverseAllNodes(doc, 0);
});


/// <summary>
/// Recursively traverses a node tree while printing the type of each node
/// with an indent depending on depth as well as the contents of all inline nodes.
/// </summary>
function traverseAllNodes(parentNode, depth)
{
  for (let childNode = parentNode.firstChild; childNode != null; childNode = childNode.nextSibling)
  {
    console.log(`${'\t'.repeat(depth)}${aw.Node.nodeTypeToString(childNode.nodeType)}`);

    // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
    if (childNode.isComposite)
    {
      traverseAllNodes(childNode.asCompositeNode(), depth + 1);
    }
    else
    {
      var text = childNode.getText().trim();
      if (text !== undefined) {
        console.log(` - \"${text}\"`);
      }
    }
  }
}
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

