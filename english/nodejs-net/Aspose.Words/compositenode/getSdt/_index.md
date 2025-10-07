---
title: CompositeNode.getSdt method
linktitle: getSdt method
articleTitle: getSdt method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getSdt method. Returns an Nth child [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node."
type: docs
weight: 170
url: /nodejs-net/aspose.words/compositenode/getSdt/
---

## getSdt(index, isDeep) {#number_boolean}

Returns an Nth child [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node.



```js
getSdt(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

