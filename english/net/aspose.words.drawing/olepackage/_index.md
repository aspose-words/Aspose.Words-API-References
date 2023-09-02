---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.OlePackage class. Allows to access OLE Package properties in C#.
type: docs
weight: 1160
url: /net/aspose.words.drawing/olepackage/
---
## OlePackage class

Allows to access OLE Package properties.

To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) documentation article.

```csharp
public class OlePackage
```

## Properties

| Name | Description |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Gets or sets OLE Package display name. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Gets or sets OLE Package file name. |

## Remarks

OLE package is a legacy and "undocumented" way to store embedded object if OLE handler is unknown. Early Windows versions such as Windows 3.1, 95 and 98 had Packager.exe application which could be used to embed any type of data into document. Now this application is excluded from Windows but MS Word and other applications still use it to embed data if OLE handler is missing or unknown.

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
