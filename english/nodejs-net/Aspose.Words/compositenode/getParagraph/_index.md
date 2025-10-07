---
title: CompositeNode.getParagraph method
linktitle: getParagraph method
articleTitle: getParagraph method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getParagraph method. Returns an Nth child [Paragraph](../../paragraph/) node."
type: docs
weight: 150
url: /nodejs-net/aspose.words/compositenode/getParagraph/
---

## getParagraph(index, isDeep) {#number_boolean}

Returns an Nth child [Paragraph](../../paragraph/) node.



```js
getParagraph(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Paragraph](../../paragraph/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Paragraph](../../paragraph/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

