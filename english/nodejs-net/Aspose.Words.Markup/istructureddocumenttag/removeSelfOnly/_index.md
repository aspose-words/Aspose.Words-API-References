---
title: IStructuredDocumentTag.removeSelfOnly method
linktitle: removeSelfOnly method
articleTitle: removeSelfOnly method
second_title: Aspose.Words for NodeJs
description: "IStructuredDocumentTag.removeSelfOnly method. Removes just this SDT node itself, but keeps the content of it inside the document tree."
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Markup/istructureddocumenttag/removeSelfOnly/
---

## removeSelfOnly() {#default}

Removes just this SDT node itself, but keeps the content of it inside the document tree.


```js
removeSelfOnly()
```

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

