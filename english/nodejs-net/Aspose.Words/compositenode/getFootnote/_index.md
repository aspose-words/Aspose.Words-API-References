---
title: CompositeNode.getFootnote method
linktitle: getFootnote method
articleTitle: getFootnote method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getFootnote method. Returns an Nth child [Footnote](../../../aspose.words.notes/footnote/) node."
type: docs
weight: 120
url: /nodejs-net/aspose.words/compositenode/getFootnote/
---

## getFootnote(index, isDeep) {#number_boolean}

Returns an Nth child [Footnote](../../../aspose.words.notes/footnote/) node.



```js
getFootnote(index: number, isDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | Zero based index of the child [Footnote](../../../aspose.words.notes/footnote/) node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children. |

### Remarks

If index is out of range, a ``null`` is returned.




### Returns

The child [Footnote](../../../aspose.words.notes/footnote/) node or ``null`` if no matching node is found.


### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

