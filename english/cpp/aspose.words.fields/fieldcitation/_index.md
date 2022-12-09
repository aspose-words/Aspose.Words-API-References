---
title: FieldCitation
second_title: Aspose.Words for C++ API Reference
description: Implements the CITATION field. To learn more, visit the  documentation article.
type: docs
weight: 274
url: /cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implements the CITATION field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Gets or sets a value that mathes the **Tag** element's value of another source to be included in the citation. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Gets or sets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumber](./get_pagenumber/)() | Gets or sets a page number associated with the citation. |
| [get_Prefix](./get_prefix/)() | Gets or sets a prefix that is prepended to the citation. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SourceTag](./get_sourcetag/)() | Gets or sets a value that mathes the **Tag** element's value of the source to insert. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_Suffix](./get_suffix/)() | Gets or sets a suffix that is appended to the citation. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Gets or sets whether the author information is suppressed from the citation. |
| [get_SuppressTitle](./get_suppresstitle/)() | Gets or sets whether the title information is suppressed from the citation. |
| [get_SuppressYear](./get_suppressyear/)() | Gets or sets whether the year information is suppressed from the citation. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_VolumeNumber](./get_volumenumber/)() | Gets or sets a volume number associated with the citation. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_AnotherSourceTag](./get_anothersourcetag/). |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_FormatLanguageId](./get_formatlanguageid/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_PageNumber](./get_pagenumber/). |
| [set_Prefix](./set_prefix/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_Prefix](./get_prefix/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_SourceTag](./get_sourcetag/). |
| [set_Suffix](./set_suffix/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_Suffix](./get_suffix/). |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Setter for [Aspose::Words::Fields::FieldCitation::get_SuppressAuthor](./get_suppressauthor/). |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Setter for [Aspose::Words::Fields::FieldCitation::get_SuppressTitle](./get_suppresstitle/). |
| [set_SuppressYear](./set_suppressyear/)(bool) | Setter for [Aspose::Words::Fields::FieldCitation::get_SuppressYear](./get_suppressyear/). |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldCitation::get_VolumeNumber](./get_volumenumber/). |
| static [Type](./type/)() |  |
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

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
