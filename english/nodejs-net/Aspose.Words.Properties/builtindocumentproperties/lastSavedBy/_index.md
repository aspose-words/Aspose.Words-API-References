---
title: BuiltInDocumentProperties.lastSavedBy property
linktitle: lastSavedBy property
articleTitle: lastSavedBy property
second_title: Aspose.Words for Node.js
description: "BuiltInDocumentProperties.lastSavedBy property. Gets or sets the name of the last author."
type: docs
weight: 150
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/lastSavedBy/
---

## BuiltInDocumentProperties.lastSavedBy property

Gets or sets the name of the last author.


```js
get lastSavedBy(): string
```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to work with document properties in the "Origin" category.

```js
// Open a document that we have created and edited using Microsoft Word.
let doc = new aw.Document(base.myDir + "Properties.docx");
let properties = doc.builtInDocumentProperties;

// The following built-in properties contain information regarding the creation and editing of this document.
// We can right-click this document in Windows Explorer and find
// these properties via "Properties" -> "Details" -> "Origin" category.
// Fields such as PRINTDATE and EDITTIME can display these values in the document body.
/*console.log(`Created using ${properties.nameOfApplication}, on ${properties.createdTime}`);
console.log(`Minutes spent editing: ${properties.totalEditingTime}`);
console.log(`Date/time last printed: ${properties.lastPrinted}`);
console.log(`Template document: ${properties.template}`);*/

// We can also change the values of built-in properties.
properties.company = "Doe Ltd.";
properties.manager = "Jane Doe";
properties.version = 5;
properties.revisionNumber++;

// Microsoft Word updates the following properties automatically when we save the document.
// To use these properties with Aspose.words, we will need to set values for them manually.
properties.lastSavedBy = "John Doe";
properties.lastSavedTime = Date.now();

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc.save(base.artifactsDir + "DocumentProperties.origin.docx");
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

