---
title: OoxmlCompliance
second_title: Aspose.Words for C++ API Reference
description: Allows to specify which OOXML specification will be used when saving in the DOCX format.
type: docs
weight: 911
url: /cpp/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enum


Allows to specify which OOXML specification will be used when saving in the DOCX format.

```cpp
enum class OoxmlCompliance
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Ecma376_2006 | 0 | ECMA-376 1st Edition, 2006. |
| Iso29500_2008_Transitional | 1 | ISO/IEC 29500:2008 Transitional compliance level. |
| Iso29500_2008_Strict | 2 | ISO/IEC 29500:2008 Strict compliance level. |


## Examples



Shows how to set an OOXML compliance specification for a saved document to adhere to. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2003);
builder->InsertImage(ImageDir + u"Transparent background logo.png");

ASSERT_EQ(ShapeMarkupLanguage::Vml, (System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_MarkupLanguage());

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(SaveFormat::Docx);

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(ShapeMarkupLanguage::Dml, (System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Shows how to configure a list to restart numbering at each section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

doc->get_Lists()->Add(ListTemplate::NumberDefault);

SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
auto options = MakeObject<OoxmlSaveOptions>();
options->set_Compliance(OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


Shows how to insert DML shapes into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder->InsertShape(ShapeType::TopCornersRounded, RelativeHorizontalPosition::Page, 100, RelativeVerticalPosition::Page, 100, 50, 50, WrapType::None);

// 2 -  Inline:
builder->InsertShape(ShapeType::DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
auto saveOptions = MakeObject<OoxmlSaveOptions>(SaveFormat::Docx);
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(ArtifactsDir + u"Shape.ShapeInsertion.docx", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
