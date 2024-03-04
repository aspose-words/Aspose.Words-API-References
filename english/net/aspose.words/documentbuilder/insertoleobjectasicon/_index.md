---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertOleObjectAsIcon method. Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension in C#.
type: docs
weight: 410
url: /net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Full path to the file. |
| isLinked | Boolean | If `true` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | String | Full path to the ICO file. If the value is `null`, Aspose.Words will use a predefined image. |
| iconCaption | String | Icon caption. If the value is `null`, Aspose.Words will use the file name. |

### Return Value

Shape node containing Ole object and inserted at the current Builder position.

## Examples

Shows how to insert an OLE object into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE objects are links to files in our local file system that can be opened by other installed applications.
// Double clicking these shapes will launch the application, and then use it to open the linked object.
// There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
// 1 -  Image taken from the local file system:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream);
}

// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
// 2 -  Icon based on the application that will open the object:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the predefined icon caption.
// 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Full path to the file. |
| progId | String | ProgId of OLE object. |
| isLinked | Boolean | If `true` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | String | Full path to the ICO file. If the value is `null`, Aspose.Words will use a predefined image. |
| iconCaption | String | Icon caption. If the value is `null`, Aspose.Words will use the file name. |

### Return Value

Shape node containing Ole object and inserted at the current Builder position.

## Examples

Shows how to insert an embedded or linked OLE object as icon into the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream containing application data. |
| progId | String | ProgId of OLE object. |
| iconFile | String | Full path to the ICO file. If the value is `null`, Aspose.Words will use a predefined image. |
| iconCaption | String | Icon caption. If the value is `null`, Aspose.Words will use the a predefined icon caption. |

### Return Value

Shape node containing Ole object and inserted at the current Builder position.

## Examples

Shows how to insert an embedded or linked OLE object as icon into the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
