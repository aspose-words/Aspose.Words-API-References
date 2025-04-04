---
title: DocumentBuilder.insertOleObject method
linktitle: insertOleObject method
articleTitle: insertOleObject method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBuilder.insertOleObject method"
type: docs
weight: 420
url: /nodejs-net/aspose.words/documentbuilder/insertOleObject/
---

## insertOleObject(stream, progId, asIcon, presentation) {#buffer_string_boolean_buffer}

Inserts an embedded OLE object from a stream into the document.


```js
insertOleObject(stream: Buffer, progId: string, asIcon: boolean, presentation: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | Stream containing application data. |
| progId | string | Programmatic Identifier of OLE object. |
| asIcon | boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Buffer | Image presentation of OLE object. If value is ``null`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insertOleObject(fileName, isLinked, asIcon, presentation) {#string_boolean_boolean_buffer}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.


```js
insertOleObject(fileName: string, isLinked: boolean, asIcon: boolean, presentation: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Full path to the file. |
| isLinked | boolean | If ``true`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Buffer | Image presentation of OLE object. If value is ``null`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insertOleObject(fileName, progId, isLinked, asIcon, presentation) {#string_string_boolean_boolean_buffer}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.


```js
insertOleObject(fileName: string, progId: string, isLinked: boolean, asIcon: boolean, presentation: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Full path to the file. |
| progId | string | ProgId of OLE object. |
| isLinked | boolean | If ``true`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Buffer | Image presentation of OLE object. If value is ``null`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## Examples

Shows how to use document builder to embed OLE objects in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a Microsoft Excel spreadsheet from the local file system
// into the document while keeping its default appearance.
let spreadsheetData = base.loadFileToBuffer(base.myDir + "Spreadsheet.xlsx");
builder.writeln("Spreadsheet Ole object:");
// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to 'progId' and uses the predefined icon caption.
builder.insertOleObject(spreadsheetData, "OleObject.xlsx", false, null);

// Insert a Microsoft Powerpoint presentation as an OLE object.
// This time, it will have an image downloaded from the web for an icon.
let powerpointData = base.loadFileToBuffer(base.myDir + "Presentation.pptx");
let imgData = base.loadFileToBuffer(base.imageDir + "Logo.jpg");

builder.insertParagraph();
builder.writeln("Powerpoint Ole object:");
builder.insertOleObject(powerpointData, "OleObject.pptx", true, imgData);

// Double-click these objects in Microsoft Word to open
// the linked files using their respective applications.
doc.save(base.artifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

Shows how to insert an OLE object into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// OLE objects are links to files in our local file system that can be opened by other installed applications.
// Double clicking these shapes will launch the application, and then use it to open the linked object.
// There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
// 1 -  Image taken from the local file system:
let imageStream = base.loadFileToBuffer(base.imageDir + "Logo.jpg");
// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to the file extension and uses the filename for the icon caption.
builder.insertOleObject(base.myDir + "Spreadsheet.xlsx", false, false, imageStream); 

// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
// 2 -  Icon based on the application that will open the object:
builder.insertOleObject(base.myDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the predefined icon caption.
// 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
builder.insertOleObjectAsIcon(base.myDir + "Presentation.pptx", false, base.imageDir + "Logo icon.ico",
  "Double click to view presentation!");

doc.save(base.artifactsDir + "DocumentBuilder.insertOleObject.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

