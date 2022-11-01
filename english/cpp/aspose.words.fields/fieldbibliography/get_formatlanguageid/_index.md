---
title: get_FormatLanguageId
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the language ID that is used to format the bibliographic sources in the document.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldbibliography/get_formatlanguageid/
---
## FieldBibliography.get_FormatLanguageId method


Gets or sets the language ID that is used to format the bibliographic sources in the document.

```cpp
System::String Aspose::Words::Fields::FieldBibliography::get_FormatLanguageId()
```


## Examples




Shows how to work with CITATION and BIBLIOGRAPHY fields. 
```cpp
// Open a document containing bibliographical sources that we can find in
// Microsoft Word via References -> Citations & Bibliography -> Manage Sources.
auto doc = MakeObject<Document>(MyDir + u"Bibliography.docx");

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Text to be cited with one source.");

// Create a citation with just the page number and the author of the referenced book.
auto fieldCitation = System::DynamicCast<FieldCitation>(builder->InsertField(FieldType::FieldCitation, true));

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
fieldCitation = System::DynamicCast<FieldCitation>(builder->InsertField(FieldType::FieldCitation, true));
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
builder->InsertBreak(BreakType::PageBreak);
auto fieldBibliography = System::DynamicCast<FieldBibliography>(builder->InsertField(FieldType::FieldBibliography, true));
fieldBibliography->set_FormatLanguageId(u"1124");

ASSERT_EQ(u" BIBLIOGRAPHY  \\l 1124", fieldBibliography->GetFieldCode());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.CITATION.docx");
```

