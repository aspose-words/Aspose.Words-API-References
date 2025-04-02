---
title: StructuredDocumentTagCollection.getByTitle method
linktitle: getByTitle method
articleTitle: getByTitle method
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagCollection.getByTitle method. Returns the first structured document tag encountered in the collection with the specified title."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagcollection/getByTitle/
---

## getByTitle(title) {#string}

Returns the first structured document tag encountered in the collection with the specified title.


```js
getByTitle(title: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| title | string | The title of structured document tag. |

### Remarks

Returns null if the structured document tag with the specified title cannot be found.




### Examples

Shows how to get structured document tag.

```js
let doc = new aw.Document(base.myDir + "Structured document tags by id.docx");

// Get the structured document tag by Id.
let sdt = doc.range.structuredDocumentTags.getById(1160505028);
console.log(sdt.isMultiSection);
console.log(sdt.title);

// Get the structured document tag or ranged tag by Title.
sdt = doc.range.structuredDocumentTags.getByTitle("Alias4");
console.log(sdt.id);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagCollection](../)

