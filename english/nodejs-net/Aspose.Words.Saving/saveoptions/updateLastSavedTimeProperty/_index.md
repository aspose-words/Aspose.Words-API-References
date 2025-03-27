---
title: SaveOptions.updateLastSavedTimeProperty property
linktitle: updateLastSavedTimeProperty property
articleTitle: updateLastSavedTimeProperty property
second_title: Aspose.Words for NodeJs
description: "SaveOptions.updateLastSavedTimeProperty property. Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../../Aspose.Words.Properties/builtindocumentproperties/lastSavedTime/) property is updated before saving."
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Saving/saveoptions/updateLastSavedTimeProperty/
---

## SaveOptions.updateLastSavedTimeProperty property

Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../../Aspose.Words.Properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.



```js
get updateLastSavedTimeProperty(): boolean
```

### Examples

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

expect(doc.builtInDocumentProperties.lastSavedTime).toEqual(new Date(2021, 5 - 1, 11, 6, 32, 0));

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "UpdateLastSavedTimeProperty" property to "true" to
// set the output document's "Last saved time" built-in property to the current date/time.
// Set the "UpdateLastSavedTimeProperty" property to "false" to
// preserve the original value of the input document's "Last saved time" built-in property.
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.updateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.save(base.artifactsDir + "OoxmlSaveOptions.lastSavedTime.docx", saveOptions);

doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.lastSavedTime.docx");
let lastSavedTimeNew = doc.builtInDocumentProperties.lastSavedTime;

if (updateLastSavedTimeProperty)
  expect(lastSavedTimeNew.getUTCDate()).toEqual(new Date().getUTCDate())
else
  expect(lastSavedTimeNew).toEqual(new Date(2021, 5 - 1, 11, 6, 32, 0));
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

