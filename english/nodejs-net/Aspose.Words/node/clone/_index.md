---
title: Node.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Node.js
description: "Node.clone method. Creates a duplicate of the node."
type: docs
weight: 430
url: /nodejs-net/aspose.words/node/clone/
---

## clone(isCloneChildren) {#boolean}

Creates a duplicate of the node.


```js
clone(isCloneChildren: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node;  false to clone only the node itself. |

### Remarks

This method serves as a copy constructor for nodes. 
The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter
specifies whether to perform copy all child nodes as well.




### Returns

The cloned node.


### Examples

Shows how to clone a composite node.

```js
let doc = new aw.Document();
let para = doc.firstSection.body.firstParagraph;
para.appendChild(new aw.Run(doc, "Hello world!"));

// Below are two ways of cloning a composite node.
// 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
let cloneWithChildren = para.clone(true).asParagraph();

expect(cloneWithChildren.hasChildNodes).toEqual(true);
expect(cloneWithChildren.getText().trim()).toEqual("Hello world!");

// 2 -  Create a clone of a node just by itself without any children.
let cloneWithoutChildren = para.clone(false).asParagraph();

expect(cloneWithoutChildren.hasChildNodes).toEqual(false);
expect(cloneWithoutChildren.getText().trim()).toEqual('');
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

