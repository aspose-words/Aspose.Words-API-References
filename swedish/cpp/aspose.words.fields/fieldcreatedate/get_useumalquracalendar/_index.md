---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar metod"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar metod. Hämtar eller anger om Um-al-Qura-kalendern ska användas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/fieldcreatedate/get_useumalquracalendar/
---
## FieldCreateDate::get_UseUmAlQuraCalendar method


Hämtar eller anger om Um-al-Qura-kalendern ska användas.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar() override
```


## Exempel



Visar hur man använder CREATEDATE-fältet för att visa dokumentets skapelsedatum/tid.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Vi kan använda CREATEDATE-fältet för att visa datum och tid för dokumentets skapelse.
// Nedan finns tre olika kalendertyper som CREATEDATE-fältet kan använda för att visa datum/tid.
// 1 -  Islamisk lunär kalender:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura-kalender:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Indisk nationell kalender:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Se även

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
