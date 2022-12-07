---
title: FieldDate
second_title: Aspose.Words for C++ API Reference
description: Implements the DATE field. To learn more, visit the  documentation article.
type: docs
weight: 391
url: /cpp/aspose.words.fields/fielddate/
---
## FieldDate class


Implements the DATE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldDate : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
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
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseLastFormat](./get_uselastformat/)() | Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() | Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() | Gets or sets whether to use the Saka Era calendar. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() | Gets or sets whether to use the Um-al-Qura calendar. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UseLastFormat](./set_uselastformat/)(bool) | Setter for [Aspose::Words::Fields::FieldDate::get_UseLastFormat](./get_uselastformat/). |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | Setter for [Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use DATE fields to display dates according to different kinds of calendars. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If we want the text in the document always to display the correct date, we can use a DATE field.
// Below are three types of cultural calendars that a DATE field can use to display a date.
// 1 -  Islamic Lunar Calendar:
auto field = System::DynamicCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura calendar:
field = System::DynamicCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Indian National Calendar:
field = System::DynamicCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Insert a DATE field and set its calendar type to the one last used by the host application.
// In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = System::DynamicCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.DATE.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
