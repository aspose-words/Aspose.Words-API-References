---
title: OleFormat.SuggestedExtension
linktitle: SuggestedExtension
articleTitle: SuggestedExtension
second_title: Aspose.Words for .NET
description: Discover the OleFormat SuggestedExtension property to easily obtain the ideal file extension for saving your embedded objects efficiently.
type: docs
weight: 120
url: /net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Gets the file extension suggested for the current embedded object if you want to save it into a file.

```csharp
public string SuggestedExtension { get; }
```

## Examples

Shows how to extract embedded OLE objects into files.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
OleFormat oleFormat = shape.OleFormat;

Assert.That(oleFormat.ProgId, Is.EqualTo("Excel.Sheet.12"));

// Our object is neither auto updating nor locked from updates.
Assert.That(oleFormat.AutoUpdate, Is.False);
Assert.That(oleFormat.IsLocked, Is.EqualTo(false));

// If we plan on saving the OLE object to a file in the local file system,
// we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
Assert.That(oleFormat.SuggestedExtension, Is.EqualTo(".xlsx"));

// Below are two ways of saving an OLE object to a file in the local file system.
// 1 -  Save it via a stream:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 -  Save it directly to a filename:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
