---
title: CompositeNode.getBuildingBlock method
linktitle: getBuildingBlock method
articleTitle: getBuildingBlock method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getBuildingBlock method. Returns an Nth child [BuildingBlock](../../buildingblock/) node."
type: docs
weight: 70
url: /nodejs-net/aspose.words/compositenode/getBuildingBlock/
---

## getBuildingBlock(index, isDeep) {#number_boolean}

Returns an Nth child [BuildingBlock](../../buildingblock/) node.



```js
getBuildingBlock(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [BuildingBlock](../../buildingblock/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [BuildingBlock](../../buildingblock/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

