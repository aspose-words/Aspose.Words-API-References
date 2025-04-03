---
title: CompositeNode.getChild method
linktitle: getChild method
articleTitle: getChild method
second_title: Aspose.Words for NodeJs
description: "CompositeNode.getChild method. Returns an Nth child node that matches the specified type."
type: docs
weight: 100
url: /nodejs-net/aspose.words/compositenode/getChild/
---

## getChild(nodeType, index, isDeep) {#nodetype_number_boolean}

Returns an Nth child node that matches the specified type.


```js
getChild(nodeType: Aspose.Words.NodeTypeindex: numberisDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | [NodeType](../../nodetype/) | Specifies the type of the child node. |
| index | number | Zero based index of the child node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. See remarks for more info. |

### Remarks

If index is out of range, a ``null`` is returned.




Note that markup nodes ([NodeType.StructuredDocumentTag](../../nodetype/#StructuredDocumentTag) and [NodeType.SmartTag](../../nodetype/#SmartTag))
are traversed even when *isDeep* =``false`` and [CompositeNode.getChild()](./#nodetype_number_boolean) is invoked for non-markup node type. For example if the first run in a para
is wrapped in a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), it will still be returned by [CompositeNode.getChild()](./#nodetype_number_boolean)([NodeType.Run](../../nodetype/#Run), 0, ``false``).


### Returns

The child node that matches the criteria or ``null`` if no matching node is found.


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
* class [CompositeNode](../)

