---
title: Document.originalFileName property
linktitle: originalFileName property
articleTitle: originalFileName property
second_title: Aspose.Words for Node.js
description: "Document.originalFileName property. Gets the original file name of the document."
type: docs
weight: 280
url: /nodejs-net/aspose.words/document/originalFileName/
---

## Document.originalFileName property

Gets the original file name of the document.


```js
get originalFileName(): string
```

### Remarks

Returns ``null`` if the document was loaded from a stream or created blank.




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
* class [Document](../)

