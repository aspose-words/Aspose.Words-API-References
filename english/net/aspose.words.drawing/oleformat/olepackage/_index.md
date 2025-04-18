---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words for .NET
description: Access OlePackage properties for OLE objects effortlessly. Get seamless integration with OLE Packages and enhance your data handling capabilities.
type: docs
weight: 80
url: /net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Provide access to [`OlePackage`](../../olepackage/) if OLE object is an OLE Package. Returns `null` otherwise.

```csharp
public OlePackage OlePackage { get; }
```

## Remarks

OLE Package is a legacy technology that allows to wrap any file format not present in the OLE registry of a Windows system into a generic package allowing to embed almost anything into a document. See [`OlePackage`](../../olepackage/) type for more info.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
