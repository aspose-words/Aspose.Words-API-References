---
title: OleFormat class
linktitle: OleFormat class
articleTitle: OleFormat class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.OleFormat class. Provides access to the data of an OLE object or ActiveX control"
type: docs
weight: 260
url: /nodejs-net/Aspose.Words.Drawing/oleformat/
---

## OleFormat class

Provides access to the data of an OLE object or ActiveX control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/nodejs-net/working-with-ole-objects/) documentation article.




### Remarks

Use the [Shape.oleFormat](../shape/oleFormat/) property to access the data of an OLE object.
You do not create instances of the [OleFormat](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [autoUpdate](./autoUpdate/) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [clsid](./clsid/) | Gets the CLSID of the OLE object. |
| [iconCaption](./iconCaption/) | Gets icon caption of OLE object. In case if the OLE object does not have an icon or a caption cannot be retrieved, returns an empty string. |
| [isLink](./isLink/) | Returns ``true`` if the OLE object is linked (when [OleFormat.sourceFullName](./sourceFullName/) is specified). |
| [isLocked](./isLocked/) | Specifies whether the link to the OLE object is locked from updates. |
| [oleControl](./oleControl/) | Gets [OleFormat.oleControl](./oleControl/) objects if this OLE object is an ActiveX control. Otherwise this property is null. |
| [oleIcon](./oleIcon/) | Gets the draw aspect of the OLE object. When ``true``, the OLE object is displayed as an icon. When ``false``, the OLE object is displayed as content. |
| [olePackage](./olePackage/) | Provide access to [OlePackage](../olepackage/) if OLE object is an OLE Package. Returns ``null`` otherwise. |
| [progId](./progId/) | Gets or sets the ProgID of the OLE object. |
| [sourceFullName](./sourceFullName/) | Gets or sets the path and name of the source file for the linked OLE object. |
| [sourceItem](./sourceItem/) | Gets or sets a string that is used to identify the portion of the source file that is being linked. |
| [suggestedExtension](./suggestedExtension/) | Gets the file extension suggested for the current embedded object if you want to save it into a file. |
| [suggestedFileName](./suggestedFileName/) | Gets the file name suggested for the current embedded object if you want to save it into a file. |

### Methods

| Name | Description |
| --- | --- |
|[ getRawData()](./getRawData/#default) | Gets OLE object raw data. |
|[ save(stream)](./save/#buffer) | Saves the data of the embedded object into the specified stream. |
|[ save(fileName)](./save/#string) | Saves the data of the embedded object into a file with the specified name. |

### Examples

Shows how to extract embedded OLE objects into files.

```js
let doc = new aw.Document(base.myDir + "OLE spreadsheet.docm");
let shape = doc.getShape(0, true);

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
let oleFormat = shape.oleFormat;

expect(oleFormat.progId).toEqual("Excel.Sheet.12");

// Our object is neither auto updating nor locked from updates.
expect(oleFormat.autoUpdate).toEqual(false);
expect(oleFormat.isLocked).toEqual(false);

// If we plan on saving the OLE object to a file in the local file system,
// we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
expect(oleFormat.suggestedExtension).toEqual(".xlsx");

// Below are two ways of saving an OLE object to a file in the local file system.
// 1 -  Save it via a stream:
let writeStream = fs.createWriteStream(base.artifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.suggestedExtension);
oleFormat.save(writeStream);
await finished(writeStream);

// 2 -  Save it directly to a filename:
oleFormat.save(base.artifactsDir + "OLE spreadsheet saved directly" + oleFormat.suggestedExtension);
```

### See Also

* module [Aspose.Words.Drawing](../)
* property [Shape.oleFormat](../shape/oleFormat/)

