---
title: FieldCreateDate
second_title: Aspose.Words for C++ API Reference
description: Implements the CREATEDATE field.
type: docs
weight: 326
url: /cpp/aspose.words.fields/fieldcreatedate/
---
## FieldCreateDate class


Implements the CREATEDATE field.

```cpp
class FieldCreateDate : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
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
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() | Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() | Gets or sets whether to use the Saka Era calendar. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() | Gets or sets whether to use the Um-al-Qura calendar. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples




Shows how to use the CREATEDATE field to display the creation date/time of the document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");
auto builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// We can use the CREATEDATE field to display the date and time of the creation of the document.
// Below are three different calendar types according to which the CREATEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::DynamicCast<FieldCreateDate>(builder->InsertField(FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura calendar:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::DynamicCast<FieldCreateDate>(builder->InsertField(FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Indian National Calendar:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::DynamicCast<FieldCreateDate>(builder->InsertField(FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.CREATEDATE.docx");
```

