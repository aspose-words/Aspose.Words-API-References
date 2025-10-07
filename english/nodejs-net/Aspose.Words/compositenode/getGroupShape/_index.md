---
title: CompositeNode.getGroupShape method
linktitle: getGroupShape method
articleTitle: getGroupShape method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getGroupShape method. Returns an Nth child [GroupShape](../../../aspose.words.drawing/groupshape/) node."
type: docs
weight: 130
url: /nodejs-net/aspose.words/compositenode/getGroupShape/
---

## getGroupShape(index, isDeep) {#number_boolean}

Returns an Nth child [GroupShape](../../../aspose.words.drawing/groupshape/) node.



```js
getGroupShape(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [GroupShape](../../../aspose.words.drawing/groupshape/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [GroupShape](../../../aspose.words.drawing/groupshape/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

