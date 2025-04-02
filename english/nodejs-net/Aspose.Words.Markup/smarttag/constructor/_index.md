---
title: SmartTag constructor
linktitle: SmartTag constructor
articleTitle: SmartTag constructor
second_title: Aspose.Words for NodeJs
description: "SmartTag constructor. Initializes a new instance of the [SmartTag](../) class."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Markup/smarttag/constructor/
---

## SmartTag(doc) {#documentbase}

Initializes a new instance of the [SmartTag](../) class.



```js
SmartTag(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../Aspose.Words/documentbase/) | The owner document. |

### Remarks

When you create a new node, you need to specify a document to which the node belongs.
A node cannot exist without a document because it depends on the document-wide structures
such as lists and styles. Although a node always belongs to a document, a node might or might
not be a part of the document tree.

When a node is created, it belongs to a document, but is not yet part of the document tree
and [Node.parentNode](../../../Aspose.Words/node/parentNode/) is null. To insert a node into the document, use the
[CompositeNode.insertAfter()](../../../Aspose.Words/compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../../Aspose.Words/compositenode/insertBefore/#node_node)
methods on the parent node.




### See Also

* module [Aspose.Words.Markup](../../)
* class [SmartTag](../)

