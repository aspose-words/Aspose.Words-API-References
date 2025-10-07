---
title: CompositeNode.getSmartTag method
linktitle: getSmartTag method
articleTitle: getSmartTag method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getSmartTag method. Returns an Nth child [SmartTag](../../../aspose.words.markup/smarttag/) node."
type: docs
weight: 210
url: /nodejs-net/aspose.words/compositenode/getSmartTag/
---

## getSmartTag(index, isDeep) {#number_boolean}

Returns an Nth child [SmartTag](../../../aspose.words.markup/smarttag/) node.



```js
getSmartTag(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [SmartTag](../../../aspose.words.markup/smarttag/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [SmartTag](../../../aspose.words.markup/smarttag/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

