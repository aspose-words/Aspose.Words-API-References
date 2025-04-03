---
title: BuiltInDocumentProperties.version property
linktitle: version property
articleTitle: version property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.version property. Represents the version number of the application that created the document."
type: docs
weight: 330
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/version/
---

## BuiltInDocumentProperties.version property

Represents the version number of the application that created the document.


```js
get version(): number
```

### Remarks

When a document was created by Microsoft Word, then high 16 bit represent
the major version and low 16 bit represent the build number.




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

