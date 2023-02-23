---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
second_title: Aspose.Words for .NET API Reference
description: OoxmlSaveOptions property. Specifies the format in which the document will be saved if this save options object is used. Can be Docx Docm Dotx Dotm or FlatOpc in C#.
type: docs
weight: 60
url: /net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can be Docx, Docm, Dotx, Dotm or FlatOpc.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

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

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* assembly [Aspose.Words](../../../)
