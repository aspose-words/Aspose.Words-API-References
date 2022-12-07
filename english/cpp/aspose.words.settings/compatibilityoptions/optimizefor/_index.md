---
title: OptimizeFor
second_title: Aspose.Words for C++ API Reference
description: Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word. Use this method to prevent MS Word from displaying "Compatibility mode" ribbon upon document loading. (Note that you may also need to set the Compliance property to Iso29500_2008_Transitional or higher.)
type: docs
weight: 963
url: /cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word. Use this method to prevent MS Word from displaying "Compatibility mode" ribbon upon document loading. (Note that you may also need to set the [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) property to [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) or higher.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
```


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


Shows how to vertically align the text contents of a text box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::TextBox, 200, 200);

// Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
// align the text in this text box with the top side of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
// align the text in this text box to the center of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
// align the text in this text box to the bottom of the shape.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2007);
doc->Save(ArtifactsDir + u"Shape.VerticalAnchor.docx");
```

## See Also

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words](../../../)
