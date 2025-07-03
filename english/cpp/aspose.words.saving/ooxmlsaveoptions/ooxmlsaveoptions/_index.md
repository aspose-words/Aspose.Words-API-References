---
title: Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions constructor
linktitle: OoxmlSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the Docx format in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Initializes a new instance of this class that can be used to save a document in the [Docx](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## Examples



Shows how to set an OOXML compliance specification for a saved document to adhere to. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## See Also

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Initializes a new instance of this class that can be used to save a document in the [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) or [FlatOpc](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Can be [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) or [FlatOpc](../../../aspose.words/saveformat/). |

## Examples



Shows how to support legacy control characters when converting to .docx. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "KeepLegacyControlChars" property to "true" to preserve
// the "ShortDateTime" legacy character while saving.
// Set the "KeepLegacyControlChars" property to "false" to remove
// the "ShortDateTime" legacy character from the output document.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
