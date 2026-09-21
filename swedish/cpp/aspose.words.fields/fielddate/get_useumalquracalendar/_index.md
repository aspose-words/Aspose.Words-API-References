---
title: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar metod"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar metod. Hämtar eller anger om Um-al-Qura‑kalendern ska användas i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fields/fielddate/get_useumalquracalendar/
---
## FieldDate::get_UseUmAlQuraCalendar method


Hämtar eller anger om Um-al-Qura-kalendern ska användas.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar() override
```


## Exempel



Visar hur man använder DATE-fält för att visa datum enligt olika typer av kalendrar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om vi vill att texten i dokumentet alltid ska visa rätt datum, kan vi använda ett DATE-fält.
// Nedan är tre typer av kulturella kalendrar som ett DATE-fält kan använda för att visa ett datum.
// 1 -  Islamisk lunär kalender:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura-kalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Indisk nationell kalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Infoga ett DATE-fält och ange dess kalendertyp till den som senast användes av värdprogrammet.
// I Microsoft Word kommer typen att vara den senast använda i dialogrutan Infoga -> Text -> Datum och tid.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Se även

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
