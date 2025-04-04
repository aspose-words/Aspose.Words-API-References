---
title: Node.customNodeId property
linktitle: customNodeId property
articleTitle: customNodeId property
second_title: Aspose.Words for Node.js
description: "Node.customNodeId property. Specifies custom node identifier."
type: docs
weight: 10
url: /nodejs-net/aspose.words/node/customNodeId/
---

## Node.customNodeId property

Specifies custom node identifier.


```js
get customNodeId(): number
```

### Remarks

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.




### Examples

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
* class [Node](../)

