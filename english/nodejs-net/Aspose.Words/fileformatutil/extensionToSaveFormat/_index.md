---
title: FileFormatUtil.extensionToSaveFormat method
linktitle: extensionToSaveFormat method
articleTitle: extensionToSaveFormat method
second_title: Aspose.Words for Node.js
description: "FileFormatUtil.extensionToSaveFormat method. Converts a file name extension into a [SaveFormat](../../saveformat/) value."
type: docs
weight: 40
url: /nodejs-net/aspose.words/fileformatutil/extensionToSaveFormat/
---

## extensionToSaveFormat(extension) {#string}

Converts a file name extension into a [SaveFormat](../../saveformat/) value.



```js
extensionToSaveFormat(extension: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| extension | string | The file extension. Can be with or without a leading dot. Case-insensitive. |

### Remarks

If the extension cannot be recognized, returns [SaveFormat.Unknown](../../saveformat/#Unknown).




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws if the parameter is ``null``. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```js
// Load a document from a file that is missing a file extension, and then detect its file format.
let docStream = base.loadFileToBuffer(base.myDir + "Word document with missing file extension");
let info = aw.FileFormatUtil.detectFileFormat(docStream);
let loadFormat = info.loadFormat;
expect(loadFormat).toEqual(aw.LoadFormat.Doc);
// Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
// 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
let fileExtension = aw.FileFormatUtil.loadFormatToExtension(loadFormat);
let saveFormat = aw.FileFormatUtil.extensionToSaveFormat(fileExtension);
// 2 -  Convert the LoadFormat directly to its SaveFormat:
saveFormat = aw.FileFormatUtil.loadFormatToSaveFormat(loadFormat);
// Load a document from the stream, and then save it to the automatically detected file extension.
let doc = new aw.Document(docStream);
expect(aw.FileFormatUtil.saveFormatToExtension(saveFormat)).toEqual(".doc");
doc.save(base.artifactsDir + "File.SaveToDetectedFileFormat" + aw.FileFormatUtil.saveFormatToExtension(saveFormat));
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatUtil](../)

