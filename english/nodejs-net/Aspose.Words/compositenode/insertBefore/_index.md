---
title: CompositeNode.insertBefore method
linktitle: insertBefore method
articleTitle: insertBefore method
second_title: Aspose.Words for Node.js
description: "CompositeNode.insertBefore method. Inserts the specified node immediately before the specified reference node."
type: docs
weight: 280
url: /nodejs-net/aspose.words/compositenode/insertBefore/
---

## insertBefore(newChild, refChild) {#node_node}

Inserts the specified node immediately before the specified reference node.


```js
insertBefore(newChild: Aspose.Words.Node, refChild: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../node/) | The [Node](../../node/) to insert. |
| refChild | [Node](../../node/) | The [Node](../../node/) that is the reference node. The *newChild* is placed before this node. |

### Remarks

If *refChild* is``null``, inserts *newChild* at the end of the list of child nodes.




If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.importNode()](../../documentbase/importNode/#node_boolean_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The inserted node.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

