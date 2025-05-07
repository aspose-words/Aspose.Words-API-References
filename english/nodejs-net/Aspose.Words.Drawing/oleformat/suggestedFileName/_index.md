---
title: OleFormat.suggestedFileName property
linktitle: suggestedFileName property
articleTitle: suggestedFileName property
second_title: Aspose.Words for Node.js
description: "OleFormat.suggestedFileName property. Gets the file name suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 130
url: /nodejs-net/aspose.words.drawing/oleformat/suggestedFileName/
---

## OleFormat.suggestedFileName property

Gets the file name suggested for the current embedded object if you want to save it into a file.


```js
get suggestedFileName(): string
```

### Examples

Shows how to get an OLE object's suggested file name.

```js
let doc = new aw.Document(base.myDir + "OLE shape.rtf");

let oleShape = doc.firstSection.body.getShape(0, true);

// OLE objects can provide a suggested filename and extension,
// which we can use when saving the object's contents into a file in the local file system.
let suggestedFileName = oleShape.oleFormat.suggestedFileName;

expect(suggestedFileName).toEqual("CSV.csv");

let writeStream = fs.createWriteStream(base.artifactsDir + suggestedFileName);
oleShape.oleFormat.save(writeStream);
await finished(writeStream);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

