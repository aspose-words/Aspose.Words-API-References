---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: Discover OoxmlSaveOptions Compliance to choose your OOXML version for output documents. Optimize your files with the default Ecma376_2006 setting.
type: docs
weight: 20
url: /net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

Specifies the OOXML version for the output document. The default value is Ecma376_2006.

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## Examples

Shows how to insert DML shapes into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 -  Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Shows how to configure a list to restart numbering at each section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.That(doc.Lists[0].IsRestartAtEachSection, Is.EqualTo(restartListAtEachSection));
```

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

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
