---
title: IStructuredDocumentTag.isMultiSection property
linktitle: isMultiSection property
articleTitle: isMultiSection property
second_title: Aspose.Words for Node.js
description: "IStructuredDocumentTag.isMultiSection property. Returns true if this instance is a ranged (multi-section) structured document tag."
type: docs
weight: 40
url: /nodejs-net/aspose.words.markup/istructureddocumenttag/isMultiSection/
---

## IStructuredDocumentTag.isMultiSection property

Returns true if this instance is a ranged (multi-section) structured document tag.


```js
get isMultiSection(): boolean
```

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
* class [IStructuredDocumentTag](../)

