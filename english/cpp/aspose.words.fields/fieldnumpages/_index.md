---
title: Aspose::Words::Fields::FieldNumPages class
linktitle: FieldNumPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldNumPages class. Implements the NUMPAGES field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 74000
url: /cpp/aspose.words.fields/fieldnumpages/
---
## FieldNumPages class


Implements the NUMPAGES field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldNumPages : public Aspose::Words::Fields::Field
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use NUMCHARS, NUMWORDS, NUMPAGES and PAGE fields to track the size of our documents. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");
auto builder = MakeObject<DocumentBuilder>(doc);

builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

// Below are three types of fields that we can use to track the size of our documents.
// 1 -  Track the character count with a NUMCHARS field:
auto fieldNumChars = System::ExplicitCast<FieldNumChars>(builder->InsertField(FieldType::FieldNumChars, true));
builder->Writeln(u" characters");

// 2 -  Track the word count with a NUMWORDS field:
auto fieldNumWords = System::ExplicitCast<FieldNumWords>(builder->InsertField(FieldType::FieldNumWords, true));
builder->Writeln(u" words");

// 3 -  Use both PAGE and NUMPAGES fields to display what page the field is on,
// and the total number of pages in the document:
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Right);
builder->Write(u"Page ");
auto fieldPage = System::ExplicitCast<FieldPage>(builder->InsertField(FieldType::FieldPage, true));
builder->Write(u" of ");
auto fieldNumPages = System::ExplicitCast<FieldNumPages>(builder->InsertField(FieldType::FieldNumPages, true));

ASSERT_EQ(u" NUMCHARS ", fieldNumChars->GetFieldCode());
ASSERT_EQ(u" NUMWORDS ", fieldNumWords->GetFieldCode());
ASSERT_EQ(u" NUMPAGES ", fieldNumPages->GetFieldCode());
ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// These fields will not maintain accurate values in real time
// while we edit the document programmatically using Aspose.Words, or in Microsoft Word.
// We need to update them every we need to see an up-to-date value.
doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
