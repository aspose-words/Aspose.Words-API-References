---
title: get_UseSakaEraCalendar
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to use the Saka Era calendar.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fielddate/get_usesakaeracalendar/
---
## FieldDate::get_UseSakaEraCalendar method


Gets or sets whether to use the Saka Era calendar.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar()
```


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

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
