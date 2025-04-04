---
title: OleFormat.isLocked property
linktitle: isLocked property
articleTitle: isLocked property
second_title: Aspose.Words for Node.js
description: "OleFormat.isLocked property. Specifies whether the link to the OLE object is locked from updates."
type: docs
weight: 50
url: /nodejs-net/aspose.words.drawing/oleformat/isLocked/
---

## OleFormat.isLocked property

Specifies whether the link to the OLE object is locked from updates.


```js
get isLocked(): boolean
```

### Remarks

The default value is ``false``.




### Examples

Shows how to extract embedded OLE objects into files.

```js
let doc = new aw.Document(base.myDir + "OLE spreadsheet.docm");
let shape = doc.getShape(0, true);

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
let oleFormat = shape.oleFormat;

expect(oleFormat.progId).toEqual("Excel.Sheet.12");

// Our object is neither auto updating nor locked from updates.
expect(oleFormat.autoUpdate).toEqual(false);
expect(oleFormat.isLocked).toEqual(false);

// If we plan on saving the OLE object to a file in the local file system,
// we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
expect(oleFormat.suggestedExtension).toEqual(".xlsx");

// Below are two ways of saving an OLE object to a file in the local file system.
// 1 -  Save it via a stream:
let writeStream = fs.createWriteStream(base.artifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.suggestedExtension);
oleFormat.save(writeStream);
await finished(writeStream);

// 2 -  Save it directly to a filename:
oleFormat.save(base.artifactsDir + "OLE spreadsheet saved directly" + oleFormat.suggestedExtension);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

