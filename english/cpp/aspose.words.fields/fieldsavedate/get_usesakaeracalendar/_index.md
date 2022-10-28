---
title: get_UseSakaEraCalendar
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to use the Saka Era calendar.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldsavedate/get_usesakaeracalendar/
---
## FieldSaveDate.get_UseSakaEraCalendar method


Gets or sets whether to use the Saka Era calendar.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar()
```


## Examples




Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");
auto builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// We can use the SAVEDATE field to display the last save operation's date and time on the document.
// The save operation that these fields refer to is the manual save in an application like Microsoft Word,
// not the document's Save method.
// Below are three different calendar types according to which the SAVEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::DynamicCast<FieldSaveDate>(builder->InsertField(FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura calendar:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::DynamicCast<FieldSaveDate>(builder->InsertField(FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Indian National calendar:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::DynamicCast<FieldSaveDate>(builder->InsertField(FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
// The document's Save method will not update this value, but we can still update it manually.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.SAVEDATE.docx");
```

