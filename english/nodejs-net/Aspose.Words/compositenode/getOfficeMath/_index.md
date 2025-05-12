---
title: CompositeNode.getOfficeMath method
linktitle: getOfficeMath method
articleTitle: getOfficeMath method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getOfficeMath method. Returns an Nth child [OfficeMath](../../../aspose.words.math/officemath/) node."
type: docs
weight: 140
url: /nodejs-net/aspose.words/compositenode/getOfficeMath/
---

## getOfficeMath(index, isDeep) {#number_boolean}

Returns an Nth child [OfficeMath](../../../aspose.words.math/officemath/) node.



```js
getOfficeMath(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [OfficeMath](../../../aspose.words.math/officemath/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [OfficeMath](../../../aspose.words.math/officemath/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

