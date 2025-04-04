---
title: OleFormat.olePackage property
linktitle: olePackage property
articleTitle: olePackage property
second_title: Aspose.Words for Node.js
description: "OleFormat.olePackage property. Provide access to [OlePackage](../../olepackage/) if OLE object is an OLE Package"
type: docs
weight: 80
url: /nodejs-net/aspose.words.drawing/oleformat/olePackage/
---

## OleFormat.olePackage property

Provide access to [OlePackage](../../olepackage/) if OLE object is an OLE Package.
Returns ``null`` otherwise.



```js
get olePackage(): Aspose.Words.Drawing.OlePackage
```

### Remarks

OLE Package is a legacy technology that allows to wrap any file format not present in the OLE registry of
a Windows system into a generic package allowing to embed almost anything into a document.
See [OlePackage](../../olepackage/) type for more info.



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

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

