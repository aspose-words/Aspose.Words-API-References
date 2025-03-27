---
title: StructuredDocumentTagCollection.getById method
linktitle: getById method
articleTitle: getById method
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagCollection.getById method. Returns the structured document tag by identifier."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagcollection/getById/
---

## getById(id) {#number}

Returns the structured document tag by identifier.


```js
getById(id: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | number | The structured document tag identifier. |

### Remarks

Returns null if the structured document tag with the specified identifier cannot be found.




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

