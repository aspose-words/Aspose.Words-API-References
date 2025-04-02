---
title: IStructuredDocumentTag.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for NodeJs
description: "IStructuredDocumentTag.title property. Specifies the friendly name associated with this SDT"
type: docs
weight: 140
url: /nodejs-net/Aspose.Words.Markup/istructureddocumenttag/title/
---

## IStructuredDocumentTag.title property

Specifies the friendly name associated with this **SDT**.
Can not be null.



```js
get title(): string
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

