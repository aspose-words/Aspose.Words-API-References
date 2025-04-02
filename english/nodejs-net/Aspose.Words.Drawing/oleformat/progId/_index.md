---
title: OleFormat.progId property
linktitle: progId property
articleTitle: progId property
second_title: Aspose.Words for NodeJs
description: "OleFormat.progId property. Gets or sets the ProgID of the OLE object."
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Drawing/oleformat/progId/
---

## OleFormat.progId property

Gets or sets the ProgID of the OLE object.


```js
get progId(): string
```

### Remarks

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be ``None``.

The default value is an empty string.




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

