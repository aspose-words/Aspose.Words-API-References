---
title: OleFormat.IconCaption
linktitle: IconCaption
articleTitle: IconCaption
second_title: Aspose.Words for .NET
description: Discover the OleFormat IconCaption property to easily retrieve and customize OLE object icon captions for enhanced document presentation.
type: docs
weight: 30
url: /net/aspose.words.drawing/oleformat/iconcaption/
---
## OleFormat.IconCaption property

Gets icon caption of OLE object.

In case if the OLE object does not have an icon or a caption cannot be retrieved, returns an empty string.

```csharp
public string IconCaption { get; }
```

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
