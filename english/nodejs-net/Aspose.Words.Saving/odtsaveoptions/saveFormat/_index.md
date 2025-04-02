---
title: OdtSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for NodeJs
description: "OdtSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Saving/odtsaveoptions/saveFormat/
---

## OdtSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.Odt](../../../Aspose.Words/saveformat/#Odt) or [SaveFormat.Ott](../../../Aspose.Words/saveformat/#Ott).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.words.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Create a new aw.Saving.OdtSaveOptions, and pass either "SaveFormat.Odt",
// or "SaveFormat.Ott" as the format to save the document in. 
let saveOptions = new aw.Saving.OdtSaveOptions(saveFormat);
saveOptions.password = "@sposeEncrypted_1145";

let extensionString = aw.FileFormatUtil.saveFormatToExtension(saveFormat);

// If we open this document with an appropriate editor,
// it will prompt us for the password we specified in the SaveOptions object.
doc.save(base.artifactsDir + "OdtSaveOptions.encrypt" + extensionString, saveOptions);

let docInfo = aw.FileFormatUtil.detectFileFormat(base.artifactsDir + "OdtSaveOptions.encrypt" + extensionString);

expect(docInfo.isEncrypted).toEqual(true);

// If we wish to open or edit this document again using Aspose.words,
// we will have to provide a LoadOptions object with the correct password to the loading constructor.
doc = new aw.Document(base.artifactsDir + "OdtSaveOptions.encrypt" + extensionString,
  new aw.Loading.LoadOptions("@sposeEncrypted_1145"));

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OdtSaveOptions](../)

