---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words for .NET
description: Discover the OlePackage FileName property to easily manage OLE package file names. Enhance your data handling with seamless integration and flexibility.
type: docs
weight: 20
url: /net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Gets or sets OLE Package file name.

```csharp
public string FileName { get; set; }
```

## Examples

Shows how insert an OLE object into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE objects allow us to open other files in the local file system using another installed application
// in our operating system by double-clicking on the shape that contains the OLE object in the document body.
// In this case, our external file will be a ZIP archive.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### See Also

* class [OlePackage](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
