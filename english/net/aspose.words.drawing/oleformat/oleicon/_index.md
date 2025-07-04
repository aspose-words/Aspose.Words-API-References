---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words for .NET
description: Discover the OleFormat OleIcon property, control OLE object display as icons or content for enhanced user experience and seamless integration in your applications.
type: docs
weight: 70
url: /net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Gets the draw aspect of the OLE object. When `true`, the OLE object is displayed as an icon. When `false`, the OLE object is displayed as content.

```csharp
public bool OleIcon { get; }
```

## Remarks

Aspose.Words does not allow to set this property to avoid confusion. If you were able to change the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original draw aspect until you edit or update the OLE object in Microsoft Word.

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
