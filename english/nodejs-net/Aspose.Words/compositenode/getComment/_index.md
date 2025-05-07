---
title: CompositeNode.getComment method
linktitle: getComment method
articleTitle: getComment method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getComment method. Returns an Nth child [Comment](../../comment/) node."
type: docs
weight: 100
url: /nodejs-net/aspose.words/compositenode/getComment/
---

## getComment(index, isDeep) {#number_boolean}

Returns an Nth child [Comment](../../comment/) node.



```js
getComment(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Comment](../../comment/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Comment](../../comment/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

