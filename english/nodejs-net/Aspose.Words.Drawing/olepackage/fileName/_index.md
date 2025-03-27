---
title: OlePackage.fileName property
linktitle: fileName property
articleTitle: fileName property
second_title: Aspose.Words for NodeJs
description: "OlePackage.fileName property. Gets or sets OLE Package file name."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Drawing/olepackage/fileName/
---

## OlePackage.fileName property

Gets or sets OLE Package file name.


```js
get fileName(): string
```

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
* class [OlePackage](../)

