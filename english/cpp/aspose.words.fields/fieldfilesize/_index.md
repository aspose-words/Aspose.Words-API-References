---
title: FieldFileSize
second_title: Aspose.Words for C++ API Reference
description: Implements the FILESIZE field.
type: docs
weight: 534
url: /cpp/aspose.words.fields/fieldfilesize/
---
## FieldFileSize class


Implements the FILESIZE field.

```cpp
class FieldFileSize : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsInKilobytes](./get_isinkilobytes/)() | Gets or sets whether to display the file size in kilobytes. |
| [get_IsInMegabytes](./get_isinmegabytes/)() | Gets or sets whether to display the file size in megabytes. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsInKilobytes](./set_isinkilobytes/)(bool) | Setter for [Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes](./get_isinkilobytes/). |
| [set_IsInMegabytes](./set_isinmegabytes/)(bool) | Setter for [Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes](./get_isinmegabytes/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

Retrieves the size of the current document's file or 0 if the size cannot be determined.

In the current implementation, uses the [OriginalFileName](../../aspose.words/document/get_originalfilename/) property to retrieve the file name used to determine the file size.

## Examples




Shows how to display the file size of a document with a FILESIZE field. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Below are three different units of measure
// with which FILESIZE fields can display the document's file size.
// 1 -  Bytes:
auto field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobytes:
builder->InsertParagraph();
field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabytes:
builder->InsertParagraph();
field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// To update the values of these fields while editing in Microsoft Word,
// we must first save the changes, and then manually update these fields.
doc->Save(ArtifactsDir + u"Field.FILESIZE.docx");
```

