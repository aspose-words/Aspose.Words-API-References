---
title: StructuredDocumentTagRangeStart.getChildNodes method
linktitle: getChildNodes method
articleTitle: getChildNodes method
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagRangeStart.getChildNodes method. Returns a live collection of child nodes that match the specified types."
type: docs
weight: 220
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagrangestart/getChildNodes/
---

## getChildNodes(nodeType, isDeep) {#nodetype_boolean}

Returns a live collection of child nodes that match the specified types.


```js
getChildNodes(nodeType: Aspose.Words.NodeTypeisDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | [NodeType](../../../Aspose.Words/nodetype/) |  |
| isDeep | boolean |  |

### Examples

Shows how to get child nodes of StructuredDocumentTagRangeStart.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");
let tag = doc.getChildNodes(aw.NodeType.StructuredDocumentTagRangeStart, true).at(0).asStructuredDocumentTagRangeStart();

console.log("StructuredDocumentTagRangeStart values:");
console.log(`\t|Child nodes count: ${tag.getChildNodes(aw.NodeType.Any, false).count}\n`);

tag.getChildNodes(aw.NodeType.Any, false).toArray().forEach(node => { console.log(`\t|Child node type: ${node.nodeType}`); });
tag.getChildNodes(aw.NodeType.Run, true).toArray().forEach(node => { console.log(`\t|Child node text: ${node.getText()}`); });
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagRangeStart](../)

