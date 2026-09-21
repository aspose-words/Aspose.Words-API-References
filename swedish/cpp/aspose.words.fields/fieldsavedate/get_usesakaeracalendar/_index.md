---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar metod"
linktitle: "get_UseSakaEraCalendar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar metod. Hämtar eller anger om Saka Era-kalendern ska användas i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldsavedate/get_usesakaeracalendar/
---
## FieldSaveDate::get_UseSakaEraCalendar method


Hämtar eller anger om Saka Era-kalendern ska användas.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar() override
```


## Exempel



Visar hur man använder SAVEDATE-fältet för att visa datum/tid för dokumentets senaste sparoperation som utförts med Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Vi kan använda SAVEDATE-fältet för att visa datum och tid för den senaste sparoperationen i dokumentet.
// Sparoperationen som dessa fält refererar till är den manuella sparningen i ett program som Microsoft Word,
// inte dokumentets Save-metod.
// Nedan är tre olika kalendertyper enligt vilka SAVEDATE-fältet kan visa datum/tid.
// 1 -  Islamisk lunär kalender:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura-kalender:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Indisk nationell kalender:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// SAVEDATE-fälten hämtar sina datum/tidsvärden från den inbyggda egenskapen LastSavedTime.
// Dokumentets Save-metod kommer inte att uppdatera detta värde, men vi kan fortfarande uppdatera det manuellt.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Se även

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
