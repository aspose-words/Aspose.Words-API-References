---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.ShapeMarkupLanguage enum, defining shape markup languages for enhanced document formatting and design flexibility.
type: docs
weight: 1670
url: /net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Specifies Markup language used for the shape.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Dml | `0` | Drawing Markup Language is used to define the shape. |
| Vml | `1` | Vector Markup Language is used to define the shape. |

## Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.That(((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage, Is.EqualTo(ShapeMarkupLanguage.Vml));

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard. 
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.That(((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage, Is.EqualTo(ShapeMarkupLanguage.Dml));
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
