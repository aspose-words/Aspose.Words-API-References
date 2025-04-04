---
title: OleFormat.oleIcon property
linktitle: oleIcon property
articleTitle: oleIcon property
second_title: Aspose.Words for Node.js
description: "OleFormat.oleIcon property. Gets the draw aspect of the OLE object"
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing/oleformat/oleIcon/
---

## OleFormat.oleIcon property

Gets the draw aspect of the OLE object. When ``true``, the OLE object is displayed as an icon.
When ``false``, the OLE object is displayed as content.



```js
get oleIcon(): boolean
```

### Remarks

Aspose.Words does not allow to set this property to avoid confusion. If you were able to change
the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original
draw aspect until you edit or update the OLE object in Microsoft Word.




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

