---
title: CompositeNode.removeSmartTags method
linktitle: removeSmartTags method
articleTitle: removeSmartTags method
second_title: Aspose.Words for Node.js
description: "CompositeNode.removeSmartTags method. Removes all [SmartTag](../../../aspose.words.markup/smarttag/) descendant nodes of the current node."
type: docs
weight: 300
url: /nodejs-net/aspose.words/compositenode/removeSmartTags/
---

## removeSmartTags() {#default}

Removes all [SmartTag](../../../aspose.words.markup/smarttag/) descendant nodes of the current node.



```js
removeSmartTags()
```

### Remarks

This method does not remove the content of the smart tags.


### Examples

Removes all smart tags from descendant nodes of a composite node.

```js
let doc = new aw.Document(base.myDir + "Smart tags.doc");

expect(doc.getChildNodes(aw.NodeType.SmartTag, true).count).toEqual(8);

doc.removeSmartTags();

expect(doc.getChildNodes(aw.NodeType.SmartTag, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

