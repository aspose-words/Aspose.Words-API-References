---
title: StructuredDocumentTagCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagCollection.remove method. Removes the structured document tag with the specified identifier."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagcollection/remove/
---

## remove(id) {#number}

Removes the structured document tag with the specified identifier.


```js
remove(id: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | number | The structured document tag identifier. |

### Examples

Shows how to remove structured document tag.

```js
let doc = new aw.Document(base.myDir + "Structured document tags.docx");

let structuredDocumentTags = doc.range.structuredDocumentTags;
for (let sdt of structuredDocumentTags) {
  console.log(sdt.title);
}

let sdt = structuredDocumentTags.getById(1691867797);
expect(sdt.id).toEqual(1691867797);

expect(structuredDocumentTags.count).toEqual(5);
// Remove the structured document tag by Id.
structuredDocumentTags.remove(1691867797);
// Remove the structured document tag at position 0.
structuredDocumentTags.removeAt(0);
expect(structuredDocumentTags.count).toEqual(3);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagCollection](../)

