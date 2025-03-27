---
title: StructuredDocumentTagCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagCollection.removeAt method. Removes a structured document tag at the specified index."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagcollection/removeAt/
---

## removeAt(index) {#number}

Removes a structured document tag at the specified index.


```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | An index into the collection. |

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

