---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.OleFormat class for seamless access to OLE objects and ActiveX controls, enhancing your document processing capabilities.
type: docs
weight: 1520
url: /net/aspose.words.drawing/oleformat/
---
## OleFormat class

Provides access to the data of an OLE object or ActiveX control.

To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) documentation article.

```csharp
public class OleFormat
```

## Properties

| Name | Description |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Gets the CLSID of the OLE object. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Gets icon caption of OLE object. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Returns `true` if the OLE object is linked (when [`SourceFullName`](./sourcefullname/) is specified). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Specifies whether the link to the OLE object is locked from updates. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Gets [`OleControl`](./olecontrol/) objects if this OLE object is an ActiveX control. Otherwise this property is null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Gets the draw aspect of the OLE object. When `true`, the OLE object is displayed as an icon. When `false`, the OLE object is displayed as content. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Provide access to [`OlePackage`](../olepackage/) if OLE object is an OLE Package. Returns `null` otherwise. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Gets or sets the ProgID of the OLE object. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Gets or sets the path and name of the source file for the linked OLE object. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Gets or sets a string that is used to identify the portion of the source file that is being linked. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Gets the file extension suggested for the current embedded object if you want to save it into a file. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Gets the file name suggested for the current embedded object if you want to save it into a file. |

## Methods

| Name | Description |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Gets OLE object data entry. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Gets OLE object raw data. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Saves the data of the embedded object into the specified stream. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Saves the data of the embedded object into a file with the specified name. |

## Remarks

Use the [`OleFormat`](../shape/oleformat/) property to access the data of an OLE object. You do not create instances of the `OleFormat` class directly.

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
