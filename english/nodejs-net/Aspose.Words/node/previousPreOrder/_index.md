---
title: Node.previousPreOrder method
linktitle: previousPreOrder method
articleTitle: previousPreOrder method
second_title: Aspose.Words for Node.js
description: "Node.previousPreOrder method. Gets the previous node according to the pre-order tree traversal algorithm."
type: docs
weight: 480
url: /nodejs-net/aspose.words/node/previousPreOrder/
---

## previousPreOrder(rootNode) {#node}

Gets the previous node according to the pre-order tree traversal algorithm.


```js
previousPreOrder(rootNode: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../) | The top node (limit) of traversal. |

### Returns

Previous node in pre-order order. Null if reached the *rootNode*.


### Examples

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

expect(doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape()).filter(s => s.hasImage).length).toEqual(9);

let curNode = doc;
while (curNode != null)
{
  let nextNode = curNode.nextPreOrder(doc);

  if (curNode.previousPreOrder(doc) != null && nextNode != null)
    expect(nextNode.previousPreOrder(doc).referenceEquals(curNode)).toBeTruthy();

  if (curNode.nodeType == aw.NodeType.Shape && curNode.asShape().hasImage)
    curNode.remove();
  curNode = nextNode;
}

expect(doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape()).filter(s => s.hasImage).length).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

