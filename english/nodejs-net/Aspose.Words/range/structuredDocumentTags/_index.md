---
title: Range.structuredDocumentTags property
linktitle: structuredDocumentTags property
articleTitle: structuredDocumentTags property
second_title: Aspose.Words for Node.js
description: "Range.structuredDocumentTags property. Returns a [Range.structuredDocumentTags](./) collection that represents all structured document tags in the range."
type: docs
weight: 50
url: /nodejs-net/aspose.words/range/structuredDocumentTags/
---

## Range.structuredDocumentTags property

Returns a [Range.structuredDocumentTags](./) collection that represents all structured document tags in the range.



```js
get structuredDocumentTags(): Aspose.Words.Markup.StructuredDocumentTagCollection
```

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

* module [Aspose.Words](../../)
* class [Range](../)

