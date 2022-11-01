---
title: FieldBibliography
second_title: Aspose.Words for C++ API Reference
description: Implements the BIBLIOGRAPHY field.
type: docs
weight: 222
url: /cpp/aspose.words.fields/fieldbibliography/
---
## FieldBibliography class


Implements the BIBLIOGRAPHY field.

```cpp
class FieldBibliography : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Gets or sets the language ID that is used to format the bibliographic sources in the document. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldBibliography::get_FormatLanguageId](./get_formatlanguageid/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

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

