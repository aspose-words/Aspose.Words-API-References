---
title: CompositeNode.getRun method
linktitle: getRun method
articleTitle: getRun method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getRun method. Returns an Nth child [Run](../../run/) node."
type: docs
weight: 160
url: /nodejs-net/aspose.words/compositenode/getRun/
---

## getRun(index, isDeep) {#number_boolean}

Returns an Nth child [Run](../../run/) node.



```js
getRun(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Run](../../run/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Run](../../run/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

