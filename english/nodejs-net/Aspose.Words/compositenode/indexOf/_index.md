---
title: CompositeNode.indexOf method
linktitle: indexOf method
articleTitle: indexOf method
second_title: Aspose.Words for Node.js
description: "CompositeNode.indexOf method. Returns the index of the specified child node in the child node array."
type: docs
weight: 240
url: /nodejs-net/aspose.words/compositenode/indexOf/
---

## indexOf(child) {#node}

Returns the index of the specified child node in the child node array.


```js
indexOf(child: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../node/) |  |

### Remarks

Returns -1 if the node is not found in the child nodes.


### Examples

Shows how to get the index of a given child node from its parent.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let body = doc.firstSection.body;

// Retrieve the index of the last paragraph in the body of the first section.
expect(body.getChildNodes(aw.NodeType.Any, false).indexOf(body.lastParagraph)).toEqual(24);
```

### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

