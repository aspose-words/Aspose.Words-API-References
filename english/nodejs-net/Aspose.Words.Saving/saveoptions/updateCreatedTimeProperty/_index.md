---
title: SaveOptions.updateCreatedTimeProperty property
linktitle: updateCreatedTimeProperty property
articleTitle: updateCreatedTimeProperty property
second_title: Aspose.Words for Node.js
description: "SaveOptions.updateCreatedTimeProperty property. Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving"
type: docs
weight: 130
url: /nodejs-net/aspose.words.saving/saveoptions/updateCreatedTimeProperty/
---

## SaveOptions.updateCreatedTimeProperty property

Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving.
Default value is ``false``;



```js
get updateCreatedTimeProperty(): boolean
```

### Examples

Shows how to update a document's "CreatedTime" property when saving.

```js
let doc = new aw.Document();
doc.builtInDocumentProperties.createdTime = new Date(2019, 12, 20);

// This flag determines whether the created time, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the created time.
let saveOptions = new aw.Saving.DocSaveOptions();
saveOptions.updateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.save(base.artifactsDir + "DocSaveOptions.updateCreatedTimeProperty.docx", saveOptions);

// Open the saved document, then verify the value of the property.
doc = new aw.Document(base.artifactsDir + "DocSaveOptions.updateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
  expect(doc.builtInDocumentProperties.createdTime).not.toEqual(new Date(2019, 12, 20));
else
  expect(doc.builtInDocumentProperties.createdTime).toEqual(new Date(2019, 12, 20));
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

