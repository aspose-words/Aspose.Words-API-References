---
title: CompositeNode.insertAfter method
linktitle: insertAfter method
articleTitle: insertAfter method
second_title: Aspose.Words for NodeJs
description: "CompositeNode.insertAfter method. Inserts the specified node immediately after the specified reference node."
type: docs
weight: 270
url: /nodejs-net/aspose.words/compositenode/insertAfter/
---

## insertAfter(newChild, refChild) {#node_node}

Inserts the specified node immediately after the specified reference node.


```js
insertAfter(newChild: Aspose.Words.Node, refChild: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../node/) | The [Node](../../node/) to insert. |
| refChild | [Node](../../node/) | The [Node](../../node/) that is the reference node. The *newChild* is placed after the*refChild*. |

### Remarks

If *refChild* is``null``, inserts *newChild* at the beginning of the list of child nodes.




If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.importNode()](../../documentbase/importNode/#node_boolean_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The inserted node.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

