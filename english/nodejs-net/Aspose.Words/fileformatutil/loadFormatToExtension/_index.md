---
title: FileFormatUtil.loadFormatToExtension method
linktitle: loadFormatToExtension method
articleTitle: loadFormatToExtension method
second_title: Aspose.Words for NodeJs
description: "FileFormatUtil.loadFormatToExtension method. Converts a load format enumerated value into a file extension"
type: docs
weight: 60
url: /nodejs-net/aspose.words/fileformatutil/loadFormatToExtension/
---

## loadFormatToExtension(loadFormat) {#loadformat}

Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.


```js
loadFormatToExtension(loadFormat: Aspose.Words.LoadFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | [LoadFormat](../../loadformat/) |  |

### Remarks

The [SaveFormat.WordML](../../saveformat/#WordML) value is converted to ".wml".




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

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

