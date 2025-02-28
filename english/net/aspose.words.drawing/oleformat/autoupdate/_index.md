---
title: OleFormat.AutoUpdate
linktitle: AutoUpdate
articleTitle: AutoUpdate
second_title: Aspose.Words for .NET
description: Discover the OleFormat AutoUpdate property in Microsoft Word, ensuring your OLE object links stay current and enhance document accuracy effortlessly.
type: docs
weight: 10
url: /net/aspose.words.drawing/oleformat/autoupdate/
---
## OleFormat.AutoUpdate property

Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.

```csharp
public bool AutoUpdate { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to extract embedded OLE objects into files.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Our object is neither auto updating nor locked from updates.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// If we plan on saving the OLE object to a file in the local file system,
// we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

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
