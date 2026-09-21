---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar-metoden"
linktitle: "get_UseSakaEraCalendar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar-metoden. Hämtar eller anger om Saka Era-kalendern ska användas i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldprintdate/get_usesakaeracalendar/
---
## FieldPrintDate::get_UseSakaEraCalendar method


Hämtar eller anger om Saka Era-kalendern ska användas.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar() override
```


## Exempel



Visar lästa PRINTDATE-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// När ett dokument skrivs ut av en skrivare eller skrivs ut som en PDF (men inte exporteras till PDF),
// PRINTDATE-fält kommer att visa utskriftsoperationens datum/tid.
// Om ingen utskrift har ägt rum, kommer dessa fält att visa "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Nedan finns tre olika kalendertyper som PRINTDATE-fältet
// kan visa datum och tid för den senaste utskriftsoperationen.
// 1 -  Islamisk lunär kalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura-kalender:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Indisk nationell kalender:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Se även

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
