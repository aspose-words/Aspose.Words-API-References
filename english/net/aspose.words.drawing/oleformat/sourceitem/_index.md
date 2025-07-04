---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: Aspose.Words for .NET
description: Discover the OleFormat SourceItem property, easily identify and manage linked portions of your source file with this essential string functionality.
type: docs
weight: 110
url: /net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

Gets or sets a string that is used to identify the portion of the source file that is being linked.

```csharp
public string SourceItem { get; set; }
```

## Remarks

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the `SourceItem` property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from the worksheet.

## Examples

Shows how to insert linked and unlinked OLE objects.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Embed a Microsoft Visio drawing into the document as an OLE object.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Insert a link to the file in the local file system and display it as an icon.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Inserting OLE objects creates shapes that store these objects.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.That(shapes.Length, Is.EqualTo(2));
Assert.That(shapes.Count(s => s.ShapeType == ShapeType.OleObject), Is.EqualTo(2));

// If a shape contains an OLE object, it will have a valid "OleFormat" property,
// which we can use to verify some aspects of the shape.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.That(oleFormat.IsLink, Is.EqualTo(false));
Assert.That(oleFormat.OleIcon, Is.EqualTo(false));

oleFormat = shapes[1].OleFormat;

Assert.That(oleFormat.IsLink, Is.EqualTo(true));
Assert.That(oleFormat.OleIcon, Is.EqualTo(true));

Assert.That(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"), Is.True);
Assert.That(oleFormat.SourceItem, Is.EqualTo(""));

Assert.That(oleFormat.IconCaption, Is.EqualTo("Microsoft Visio drawing.vsd"));

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// If the object contains OLE data, we can access it using a stream.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.That(oleEntryBytes.Length, Is.EqualTo(76));
}
```

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
