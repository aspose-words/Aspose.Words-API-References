---
title: IStructuredDocumentTag.getChildNodes method
linktitle: getChildNodes method
articleTitle: getChildNodes method
second_title: Aspose.Words for NodeJs
description: "IStructuredDocumentTag.getChildNodes method. Returns a live collection of child nodes that match the specified types."
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Markup/istructureddocumenttag/getChildNodes/
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

Shows how to remove structured document tag, but keeps content inside.

```js
let doc = new aw.Document(base.myDir + "Structured document tags.docx");

// This collection provides a unified interface for accessing ranged and non-ranged structured tags. 
let sdts = doc.range.structuredDocumentTags;
expect(sdts.count).toEqual(5);

// Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
for (let sdt of sdts)
{
  if (sdt.getChildNodes(aw.NodeType.Any, false).count > 0)
    sdt.removeSelfOnly();
}

sdts = doc.range.structuredDocumentTags;
expect(sdts.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [IStructuredDocumentTag](../)

