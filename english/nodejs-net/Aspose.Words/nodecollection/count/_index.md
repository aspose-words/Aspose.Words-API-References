---
title: NodeCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "NodeCollection.count property. Gets the number of nodes in the collection."
type: docs
weight: 10
url: /nodejs-net/aspose.words/nodecollection/count/
---

## NodeCollection.count property

Gets the number of nodes in the collection.


```js
get count(): number
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

Shows how to traverse through a composite node's collection of child nodes.

```js
let doc = new aw.Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
let paragraph = doc.getParagraph(0, true);
paragraph.appendChild(new aw.Run(doc, "Hello world! "));

let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
shape.width = 200;
shape.height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.customNodeId = 100;
shape.wrapType = aw.Drawing.WrapType.Inline;
paragraph.appendChild(shape);

paragraph.appendChild(new aw.Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
let children = paragraph.getChildNodes(aw.NodeType.Any, false);

expect(paragraph.getChildNodes(aw.NodeType.Any, false).count).toEqual(3);

for (let child of children)
  switch (child.nodeType)
  {
    case aw.NodeType.Run:
      console.log("Run contents:");
      console.log(`\t\"${child.getText().trim()}\"`);
      break;
    case aw.NodeType.Shape:
      let childShape = child.asShape();
      console.log("Shape:");
      console.log(`\t${childShape.shapeType}, ${childShape.width}x${childShape.height}`);
      expect(shape.customNodeId).toEqual(100);
      break;
  }
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

