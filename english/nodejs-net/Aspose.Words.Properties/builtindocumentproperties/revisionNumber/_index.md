---
title: BuiltInDocumentProperties.revisionNumber property
linktitle: revisionNumber property
articleTitle: revisionNumber property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.revisionNumber property. Gets or sets the document revision number."
type: docs
weight: 230
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/revisionNumber/
---

## BuiltInDocumentProperties.revisionNumber property

Gets or sets the document revision number.


```js
get revisionNumber(): number
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

Shows how to work with REVNUM fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Current revision #");

// Insert a REVNUM field, which displays the document's current revision number property.
let field = builder.insertField(aw.Fields.FieldType.FieldRevisionNum, true).asFieldRevNum();

expect(field.getFieldCode()).toEqual(" REVNUM ");
expect(field.result).toEqual("1");
expect(doc.builtInDocumentProperties.revisionNumber).toEqual(1);

// This property counts how many times a document has been saved in Microsoft Word,
// and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
// via Properties -> Details. We can update this property manually.
doc.builtInDocumentProperties.revisionNumber++;
expect(field.result).toEqual("1");
field.update();

expect(field.result).toEqual("2");
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

