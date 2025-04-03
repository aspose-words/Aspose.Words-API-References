---
title: DocumentProperty.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "DocumentProperty.name property. Returns the name of the property."
type: docs
weight: 30
url: /nodejs-net/aspose.words.properties/documentproperty/name/
---

## DocumentProperty.name property

Returns the name of the property.


```js
get name(): string
```

### Remarks

Cannot be ``null`` and cannot be an empty string.




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

* module [Aspose.Words.Properties](../../)
* class [DocumentProperty](../)

