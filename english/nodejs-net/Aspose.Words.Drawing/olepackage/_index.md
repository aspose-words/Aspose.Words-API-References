---
title: OlePackage class
linktitle: OlePackage class
articleTitle: OlePackage class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.OlePackage class. Allows to access OLE Package properties"
type: docs
weight: 270
url: /nodejs-net/aspose.words.drawing/olepackage/
---

## OlePackage class

Allows to access OLE Package properties.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/nodejs-net/working-with-ole-objects/) documentation article.




### Remarks

OLE package is a legacy and "undocumented" way to store embedded object if OLE handler is unknown.
Early Windows versions such as Windows 3.1, 95 and 98 had Packager.exe application which could be used to embed any type of data into document.
Now this application is excluded from Windows but MS Word and other applications still use it to embed data if OLE handler is missing or unknown.


### Properties

| Name | Description |
| --- | --- |
| [displayName](./displayName/) | Gets or sets OLE Package display name. |
| [fileName](./fileName/) | Gets or sets OLE Package file name. |

### Examples

Shows how insert an OLE object into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// OLE objects allow us to open other files in the local file system using another installed application
// in our operating system by double-clicking on the shape that contains the OLE object in the document body.
// In this case, our external file will be a ZIP archive.
let readStream = fs.createReadStream(base.databaseDir + "cat001.zip");
let shape = builder.insertOleObject(readStream, "Package", true, null);
shape.oleFormat.olePackage.fileName = "Package file name.zip";
shape.oleFormat.olePackage.displayName = "Package display name.zip";

doc.save(base.artifactsDir + "Shape.InsertOlePackage.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)

