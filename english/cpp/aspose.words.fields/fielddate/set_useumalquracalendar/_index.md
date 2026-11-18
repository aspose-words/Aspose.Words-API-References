---
title: Aspose::Words::Fields::FieldDate::set_UseUmAlQuraCalendar method
linktitle: set_UseUmAlQuraCalendar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDate::set_UseUmAlQuraCalendar method. Sets whether to use the Um-al-Qura calendar in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.fields/fielddate/set_useumalquracalendar/
---
## FieldDate::set_UseUmAlQuraCalendar method


Sets whether to use the Um-al-Qura calendar.

```cpp
void Aspose::Words::Fields::FieldDate::set_UseUmAlQuraCalendar(bool value)
```

## Examples


Shows how to use DATE fields to display dates according to different kinds of calendars.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// If we want the text in the document always to display the correct date, we can use a DATE field.
// Below are three types of cultural calendars that a DATE field can use to display a date.
// 1 -  Islamic Lunar Calendar:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(field->GetFieldCode(), u" DATE  \\h");
builder->Writeln();

// 2 -  Umm al-Qura calendar:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(field->GetFieldCode(), u" DATE  \\u");
builder->Writeln();

// 3 -  Indian National Calendar:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(field->GetFieldCode(), u" DATE  \\s");
builder->Writeln();

// Insert a DATE field and set its calendar type to the one last used by the host application.
// In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(field->GetFieldCode(), u" DATE  \\l");
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```
## See Also

* [get_UseUmAlQuraCalendar](../get_useumalquracalendar/)

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
