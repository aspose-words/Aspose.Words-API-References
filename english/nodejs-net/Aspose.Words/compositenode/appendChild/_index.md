---
title: CompositeNode.appendChild method
linktitle: appendChild method
articleTitle: appendChild method
second_title: Aspose.Words for Node.js
description: "CompositeNode.appendChild method. Adds the specified node to the end of the list of child nodes for this node."
type: docs
weight: 80
url: /nodejs-net/aspose.words/compositenode/appendChild/
---

## appendChild(newChild) {#node}

Adds the specified node to the end of the list of child nodes for this node.


```js
appendChild(newChild: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.importNode()](../../documentbase/importNode/#node_boolean_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

