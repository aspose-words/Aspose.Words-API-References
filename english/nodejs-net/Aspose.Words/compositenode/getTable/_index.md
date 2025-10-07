---
title: CompositeNode.getTable method
linktitle: getTable method
articleTitle: getTable method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getTable method. Returns an Nth child [Table](../../table/) node."
type: docs
weight: 220
url: /nodejs-net/aspose.words/compositenode/getTable/
---

## getTable(index, isDeep) {#number_boolean}

Returns an Nth child [Table](../../table/) node.



```js
getTable(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Table](../../table/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Table](../../table/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

