---
title: OleFormat.getRawData method
linktitle: getRawData method
articleTitle: getRawData method
second_title: Aspose.Words for NodeJs
description: "OleFormat.getRawData method. Gets OLE object raw data."
type: docs
weight: 140
url: /nodejs-net/Aspose.Words.Drawing/oleformat/getRawData/
---

## getRawData() {#default}

Gets OLE object raw data.


```js
getRawData()
```

### Examples

Shows how to access the raw data of an embedded OLE object.

```js
let doc = new aw.Document(base.myDir + "OLE objects.docx");

for (let shape of doc.getChildNodes(aw.NodeType.Shape, true))
{
  let oleFormat = shape.oleFormat;
  if (oleFormat != null)
  {
    console.log(`This is ${(oleFormat.isLink ? "a linked" : "an embedded")} object`);
    let oleRawData = oleFormat.getRawData();

    expect(oleRawData.length).toEqual(24576);
  }
}
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

