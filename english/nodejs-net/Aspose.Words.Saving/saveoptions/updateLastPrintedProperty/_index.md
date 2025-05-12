---
title: SaveOptions.updateLastPrintedProperty property
linktitle: updateLastPrintedProperty property
articleTitle: updateLastPrintedProperty property
second_title: Aspose.Words for Node.js
description: "SaveOptions.updateLastPrintedProperty property. Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving."
type: docs
weight: 150
url: /nodejs-net/aspose.words.saving/saveoptions/updateLastPrintedProperty/
---

## SaveOptions.updateLastPrintedProperty property

Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.



```js
get updateLastPrintedProperty(): boolean
```

### Examples

Shows how to update a document's "Last printed" property when saving.

```js
let doc = new aw.Document();
doc.builtInDocumentProperties.lastPrinted = new Date(2019, 12, 20);

// This flag determines whether the last printed date, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the print date.
let saveOptions = new aw.Saving.DocSaveOptions();
saveOptions.updateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
// It can also be displayed in the document's body by using a PRINTDATE field.
doc.save(base.artifactsDir + "DocSaveOptions.updateLastPrintedProperty.doc", saveOptions);

// Open the saved document, then verify the value of the property.
doc = new aw.Document(base.artifactsDir + "DocSaveOptions.updateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
  expect(doc.builtInDocumentProperties.lastPrinted).not.toEqual(new Date(2019, 12, 20));
else
  expect(doc.builtInDocumentProperties.lastPrinted).toEqual(new Date(2019, 12, 20));
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

