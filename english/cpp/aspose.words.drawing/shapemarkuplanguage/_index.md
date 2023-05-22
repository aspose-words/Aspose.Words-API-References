---
title: Aspose::Words::Drawing::ShapeMarkupLanguage enum
linktitle: ShapeMarkupLanguage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeMarkupLanguage enum. Specifies Markup language used for the shape in C++.'
type: docs
weight: 37000
url: /cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


Specifies [Markup](../../aspose.words.markup/) language used for the shape.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Markup](../../aspose.words.markup/) Language is used to define the shape. |
| Vml | 1 | Vector [Markup](../../aspose.words.markup/) Language is used to define the shape. |


## Examples



Shows how to set an OOXML compliance specification for a saved document to adhere to. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2003);
builder->InsertImage(ImageDir + u"Transparent background logo.png");

ASSERT_EQ(ShapeMarkupLanguage::Vml, (System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_MarkupLanguage());

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(SaveFormat::Docx);

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(ShapeMarkupLanguage::Dml, (System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
