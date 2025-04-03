---
title: OleFormat.sourceItem property
linktitle: sourceItem property
articleTitle: sourceItem property
second_title: Aspose.Words for NodeJs
description: "OleFormat.sourceItem property. Gets or sets a string that is used to identify the portion of the source file that is being linked."
type: docs
weight: 110
url: /nodejs-net/aspose.words.drawing/oleformat/sourceItem/
---

## OleFormat.sourceItem property

Gets or sets a string that is used to identify the portion of the source file that is being linked.


```js
get sourceItem(): string
```

### Remarks

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [OleFormat.sourceItem](./)
property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from
the worksheet.




### Examples

Shows how to insert linked and unlinked OLE objects.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Embed a Microsoft Visio drawing into the document as an OLE object.
builder.insertOleObject(base.imageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Insert a link to the file in the local file system and display it as an icon.
builder.insertOleObject(base.imageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Inserting OLE objects creates shapes that store these objects.
let shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());

expect(shapes.length).toEqual(2);
expect(shapes.filter(s => s.shapeType == aw.Drawing.ShapeType.OleObject).length).toEqual(2);

// If a shape contains an OLE object, it will have a valid "OleFormat" property,
// which we can use to verify some aspects of the shape.
let oleFormat = shapes.at(0).oleFormat;

expect(oleFormat.isLink).toEqual(false);
expect(oleFormat.oleIcon).toEqual(false);

oleFormat = shapes.at(1).oleFormat;

expect(oleFormat.isLink).toEqual(true);
expect(oleFormat.oleIcon).toEqual(true);

expect(oleFormat.sourceFullName.endsWith(`Images${path.sep}Microsoft Visio drawing.vsd`)).toEqual(true);
expect(oleFormat.sourceItem).toEqual("");

expect(oleFormat.iconCaption).toEqual("Microsoft Visio drawing.vsd");

doc.save(base.artifactsDir + "Shape.OleLinks.docx");

// If the object contains OLE data, we can access it using a stream.
/*using (Stream stream = oleFormat.getOleEntry("\x0001CompObj"))
{
  expect(stream.length).toEqual(76);
}*/
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

