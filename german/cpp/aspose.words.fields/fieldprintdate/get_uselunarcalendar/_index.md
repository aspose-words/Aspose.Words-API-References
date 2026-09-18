---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar Methode"
linktitle: "get_UseLunarCalendar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar Methode. Gibt an oder legt fest, ob der Hijri-Lunar- oder Hebrew-Lunar-Kalender in C++ verwendet wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldprintdate/get_uselunarcalendar/
---
## FieldPrintDate::get_UseLunarCalendar method


Liest oder setzt, ob der islamische Mondkalender oder der hebräische Mondkalender verwendet wird.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar() override
```


## Beispiele



Zeigt gelesene PRINTDATE-Felder an.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Wenn ein Dokument von einem Drucker oder als PDF gedruckt wird (aber nicht als PDF exportiert wird),
// Zeigen die PRINTDATE-Felder das Datum/Uhrzeit des Druckvorgangs an.
// Wenn kein Druckvorgang stattgefunden hat, zeigen diese Felder "0/0/0000" an.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das PRINTDATE-Feld
// das Datum und die Uhrzeit des letzten Druckvorgangs anzeigen kann.
// 1 -  Islamischer Mondkalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al‑Qura‑Kalender:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Indischer Nationalkalender:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Siehe auch

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
