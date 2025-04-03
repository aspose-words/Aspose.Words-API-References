---
title: Cell constructor
linktitle: Cell constructor
articleTitle: Cell constructor
second_title: Aspose.Words for NodeJs
description: "Cell constructor. Initializes a new instance of the [Cell](../) class."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Tables/cell/constructor/
---

## Cell(doc) {#documentbase}

Initializes a new instance of the [Cell](../) class.



```js
Cell(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Cell](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../../aspose.words/node/parentNode/) is ``null``.

To append [Cell](../) to the document use [CompositeNode.insertAfter()](../../../aspose.words/compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../../aspose.words/compositenode/insertBefore/#node_node)
on the row where you want the cell inserted.




### See Also

* module [Aspose.Words.Tables](../../)
* class [Cell](../)

