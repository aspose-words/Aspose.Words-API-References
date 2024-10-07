---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertOleObject method. Inserts an embedded OLE object from a stream into the document in C#.
type: docs
weight: 420
url: /net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

Inserts an embedded OLE object from a stream into the document.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream containing application data. |
| progId | String | Programmatic Identifier of OLE object. |
| asIcon | Boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Stream | Image presentation of OLE object. If value is `null` Aspose.Words will use one of the predefined images. |

### Return Value

Shape node containing Ole object and inserted at the current Builder position.

## Examples

Shows how to use document builder to embed OLE objects in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a Microsoft Excel spreadsheet from the local file system
// into the document while keeping its default appearance.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
    // the icon according to 'progId' and uses the predefined icon caption.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Insert a Microsoft Powerpoint presentation as an OLE object.
// This time, it will have an image downloaded from the web for an icon.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

    using (MemoryStream imageStream = new MemoryStream(imgBytes))
    {
        builder.InsertParagraph();
        builder.Writeln("Powerpoint Ole object:");
        builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
    }
}

// Double-click these objects in Microsoft Word to open
// the linked files using their respective applications.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Full path to the file. |
| isLinked | Boolean | If `true` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | Boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Stream | Image presentation of OLE object. If value is `null` Aspose.Words will use one of the predefined images. |

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

## InsertOleObject(*string, string, bool, bool, Stream*) {#insertoleobject_2}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Full path to the file. |
| progId | String | ProgId of OLE object. |
| isLinked | Boolean | If `true` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | Boolean | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | Stream | Image presentation of OLE object. If value is `null` Aspose.Words will use one of the predefined images. |

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
