---
title: CompositeNode.getShape method
linktitle: getShape method
articleTitle: getShape method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getShape method. Returns an Nth child [Shape](../../../aspose.words.drawing/shape/) node."
type: docs
weight: 200
url: /nodejs-net/aspose.words/compositenode/getShape/
---

## getShape(index, isDeep) {#number_boolean}

Returns an Nth child [Shape](../../../aspose.words.drawing/shape/) node.



```js
getShape(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Shape](../../../aspose.words.drawing/shape/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Shape](../../../aspose.words.drawing/shape/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

