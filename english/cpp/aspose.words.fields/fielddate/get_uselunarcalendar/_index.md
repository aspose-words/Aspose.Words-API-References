---
title: Aspose::Words::Fields::FieldDate::get_UseLunarCalendar method
linktitle: get_UseLunarCalendar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDate::get_UseLunarCalendar method. Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fielddate/get_uselunarcalendar/
---
## FieldDate::get_UseLunarCalendar method


Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLunarCalendar() override
```


## Examples



Shows how to use DATE fields to display dates according to different kinds of calendars. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// If we want the text in the document always to display the correct date, we can use a DATE field.
// Below are three types of cultural calendars that a DATE field can use to display a date.
// 1 -  Islamic Lunar Calendar:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura calendar:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Indian National Calendar:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Insert a DATE field and set its calendar type to the one last used by the host application.
// In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## See Also

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
