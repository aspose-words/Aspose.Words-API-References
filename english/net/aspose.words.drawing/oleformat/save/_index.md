---
title: Save
second_title: Aspose.Words for .NET API Reference
description: OleFormat method. Saves the data of the embedded object into the specified stream in C#.
type: docs
weight: 160
url: /net/aspose.words.drawing/oleformat/save/
---
## Save(Stream) {#save}

Saves the data of the embedded object into the specified stream.

```csharp
public void Save(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Where to save the object data. |

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Throws if you attempt to save a linked object. |

## Remarks

It is the responsibility of the caller to dispose the stream.

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
* namespace [Aspose.Words.Drawing](../../oleformat/)
* assembly [Aspose.Words](../../../)

---

## Save(string) {#save_1}

Saves the data of the embedded object into a file with the specified name.

```csharp
public void Save(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Name of the file to save the OLE object data. |

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Throws if you attempt to save a linked object. |

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
* namespace [Aspose.Words.Drawing](../../oleformat/)
* assembly [Aspose.Words](../../../)
