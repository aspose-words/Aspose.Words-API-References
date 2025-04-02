---
title: DocumentBuilder.insertOleObjectAsIcon method
linktitle: insertOleObjectAsIcon method
articleTitle: insertOleObjectAsIcon method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertOleObjectAsIcon method"
type: docs
weight: 430
url: /nodejs-net/Aspose.Words/documentbuilder/insertOleObjectAsIcon/
---

## insertOleObjectAsIcon(fileName, isLinked, iconFile, iconCaption) {#string_boolean_string_string}

Inserts an embedded or linked OLE object as icon into the document.
Allows to specify icon file and caption. Detects OLE object type using file extension.


```js
insertOleObjectAsIcon(fileName: stringisLinked: booleaniconFile: stringiconCaption: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Full path to the file. |
| isLinked | boolean | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | string | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| iconCaption | string | Icon caption. If the value is ``None``, Aspose.Words will use the file name. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insertOleObjectAsIcon(fileName, progId, isLinked, iconFile, iconCaption) {#string_string_boolean_string_string}

Inserts an embedded or linked OLE object as icon into the document.
Allows to specify icon file and caption. Detects OLE object type using given progID parameter.


```js
insertOleObjectAsIcon(fileName: stringprogId: stringisLinked: booleaniconFile: stringiconCaption: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Full path to the file. |
| progId | string | ProgId of OLE object. |
| isLinked | boolean | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | string | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| iconCaption | string | Icon caption. If the value is ``None``, Aspose.Words will use the file name. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insertOleObjectAsIcon(stream, progId, iconFile, iconCaption) {#buffer_string_string_string}

Inserts an embedded OLE object as icon from a stream into the document.
Allows to specify icon file and caption. Detects OLE object type using given progID parameter.


```js
insertOleObjectAsIcon(stream: BufferprogId: stringiconFile: stringiconCaption: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | Stream containing application data. |
| progId | string | ProgId of OLE object. |
| iconFile | string | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| iconCaption | string | Icon caption. If the value is ``None``, Aspose.Words will use the a predefined icon caption. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## Examples

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

Shows how to insert an embedded or linked OLE object as icon into the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder.insertOleObjectAsIcon(base.myDir + "Presentation.pptx", "Package", false, base.imageDir + "Logo icon.ico", "My embedded file");

builder.insertBreak(aw.BreakType.LineBreak);

let stream = base.loadFileToBuffer(base.myDir + "Presentation.pptx");
// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to the file extension and uses the filename for the icon caption.
let shape = builder.insertOleObjectAsIcon(stream, "PowerPoint.Application", base.imageDir + "Logo icon.ico",
  "My embedded file stream");

let setOlePackage = shape.oleFormat.olePackage;
setOlePackage.fileName = "Presentation.pptx";
setOlePackage.displayName = "Presentation.pptx";

doc.save(base.artifactsDir + "DocumentBuilder.insertOleObjectAsIcon.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

