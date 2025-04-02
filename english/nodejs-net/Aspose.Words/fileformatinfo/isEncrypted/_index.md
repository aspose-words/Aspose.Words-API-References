---
title: FileFormatInfo.isEncrypted property
linktitle: isEncrypted property
articleTitle: isEncrypted property
second_title: Aspose.Words for NodeJs
description: "FileFormatInfo.isEncrypted property. Returns ``True`` if the document is encrypted and requires a password to open."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/fileformatinfo/isEncrypted/
---

## FileFormatInfo.isEncrypted property

Returns ``True`` if the document is encrypted and requires a password to open.



```js
get isEncrypted(): boolean
```

### Remarks

This property exists to help you sort documents that are encrypted from those that are not.
If you attempt to load an encrypted document using Aspose.Words without supplying a password an
exception will be thrown. You can use this property to detect whether a document requires a password
and take some action before loading a document, for example, prompt the user for a password.




### Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```js
let doc = new aw.Document();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
let saveOptions = new aw.Saving.OdtSaveOptions(aw.SaveFormat.Odt);
saveOptions.password = "MyPassword";

doc.save(base.artifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
let info = aw.FileFormatUtil.detectFileFormat(base.artifactsDir + "File.DetectDocumentEncryption.odt");

expect(aw.FileFormatUtil.loadFormatToExtension(info.loadFormat)).toEqual(".odt");
expect(info.isEncrypted).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.loadFormat](../loadFormat/)

