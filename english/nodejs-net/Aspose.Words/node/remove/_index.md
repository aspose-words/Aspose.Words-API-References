---
title: Node.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for NodeJs
description: "Node.remove method. Removes itself from the parent."
type: docs
weight: 500
url: /nodejs-net/aspose.words/node/remove/
---

## remove() {#default}

Removes itself from the parent.


```js
remove()
```

### Examples

Shows how to remove all child nodes of a specific type from a composite node.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(2);

let curNode = doc.firstSection.body.firstChild;

while (curNode != null)
{
  // Save the next sibling node as a variable in case we want to move to it after deleting this node.
  let nextNode = curNode.nextSibling;

  // A section body can contain Paragraph and Table nodes.
  // If the node is a Table, remove it from the parent.
  if (curNode.nodeType == aw.NodeType.Table)
    curNode.remove();

  curNode = nextNode;
}

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(0);
```

Shows how to delete all shapes with images from a document.

```js
let doc = new aw.Document(base.myDir + "Images.docx");
let shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());

expect(shapes.filter(s => s.hasImage).length).toEqual(9);

for (let shape of shapes)
  if (shape.hasImage) 
    shape.remove();

shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());
expect(shapes.filter(s => s.hasImage).length).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

