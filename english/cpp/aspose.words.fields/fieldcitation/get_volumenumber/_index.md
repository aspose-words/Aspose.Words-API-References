---
title: Aspose::Words::Fields::FieldCitation::get_VolumeNumber method
linktitle: get_VolumeNumber
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldCitation::get_VolumeNumber method. Gets or sets a volume number associated with the citation in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.fields/fieldcitation/get_volumenumber/
---
## FieldCitation::get_VolumeNumber method


Gets or sets a volume number associated with the citation.

```cpp
System::String Aspose::Words::Fields::FieldCitation::get_VolumeNumber()
```


## Examples



Shows how to work with CITATION and BIBLIOGRAPHY fields. 
```cpp
// Open a document containing bibliographical sources that we can find in
// Microsoft Word via References -> Citations & Bibliography -> Manage Sources.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bibliography.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Text to be cited with one source.");

// Create a citation with just the page number and the author of the referenced book.
auto fieldCitation = System::ExplicitCast<Aspose::Words::Fields::FieldCitation>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCitation, true));

// We refer to sources using their tag names.
fieldCitation->set_SourceTag(u"Book1");
fieldCitation->set_PageNumber(u"85");
fieldCitation->set_SuppressAuthor(false);
fieldCitation->set_SuppressTitle(true);
fieldCitation->set_SuppressYear(true);

ASSERT_EQ(u" CITATION  Book1 \\p 85 \\t \\y", fieldCitation->GetFieldCode());

// Create a more detailed citation which cites two sources.
builder->InsertParagraph();
builder->Write(u"Text to be cited with two sources.");
fieldCitation = System::ExplicitCast<Aspose::Words::Fields::FieldCitation>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCitation, true));
fieldCitation->set_SourceTag(u"Book1");
fieldCitation->set_AnotherSourceTag(u"Book2");
fieldCitation->set_FormatLanguageId(u"en-US");
fieldCitation->set_PageNumber(u"19");
fieldCitation->set_Prefix(u"Prefix ");
fieldCitation->set_Suffix(u" Suffix");
fieldCitation->set_SuppressAuthor(false);
fieldCitation->set_SuppressTitle(false);
fieldCitation->set_SuppressYear(false);
fieldCitation->set_VolumeNumber(u"VII");

ASSERT_EQ(u" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation->GetFieldCode());

// We can use a BIBLIOGRAPHY field to display all the sources within the document.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto fieldBibliography = System::ExplicitCast<Aspose::Words::Fields::FieldBibliography>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBibliography, true));
fieldBibliography->set_FormatLanguageId(u"5129");
fieldBibliography->set_FilterLanguageId(u"5129");
fieldBibliography->set_SourceTag(u"Book2");

ASSERT_EQ(u" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CITATION.docx");
```

## See Also

* Class [FieldCitation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
