---
title: Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar method
linktitle: get_UseUmAlQuraCalendar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar method. Gets or sets whether to use the Um-al-Qura calendar in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fields/fieldcreatedate/get_useumalquracalendar/
---
## FieldCreateDate::get_UseUmAlQuraCalendar method


Gets or sets whether to use the Um-al-Qura calendar.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar() override
```


## Examples



Shows how to use the CREATEDATE field to display the creation date/time of the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// We can use the CREATEDATE field to display the date and time of the creation of the document.
// Below are three different calendar types according to which the CREATEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura calendar:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Indian National Calendar:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## See Also

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
