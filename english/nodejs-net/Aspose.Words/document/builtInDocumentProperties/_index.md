---
title: Document.builtInDocumentProperties property
linktitle: builtInDocumentProperties property
articleTitle: builtInDocumentProperties property
second_title: Aspose.Words for Node.js
description: "Document.builtInDocumentProperties property. Returns a collection that represents all the built-in document properties of the document."
type: docs
weight: 50
url: /nodejs-net/aspose.words/document/builtInDocumentProperties/
---

## Document.builtInDocumentProperties property

Returns a collection that represents all the built-in document properties of the document.


```js
get builtInDocumentProperties(): Aspose.Words.Properties.BuiltInDocumentProperties
```

### Examples

Shows how to work with built-in document properties.

```js
let doc = new aw.Document(base.myDir + "Properties.docx");

// The "Document" object contains some of its metadata in its members.
//console.log(`Document filename:\n\t \"${doc.originalFileName}\"`);

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
/*console.log("Built-in Properties:");
for (let docProperty of doc.builtInDocumentProperties)
{
  console.log(docProperty.name);
  console.log(`\tType:\t${docProperty.type}`);
  console.log(`\tValue:\t\"${docProperty.toString()}\"`);
}*/
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

