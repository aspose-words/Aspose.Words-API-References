---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar metodo"
linktitle: "get_UseLunarCalendar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar metodo. Ottiene o imposta se utilizzare il calendario lunare Hijri o il calendario lunare ebraico in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldprintdate/get_uselunarcalendar/
---
## FieldPrintDate::get_UseLunarCalendar method


Ottiene o imposta se utilizzare il calendario lunare Hijri o il calendario lunare ebraico.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar() override
```


## Esempi



Mostra i campi PRINTDATE letti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Quando un documento viene stampato da una stampante o stampato come PDF (ma non esportato in PDF),
// I campi PRINTDATE mostreranno la data/ora dell'operazione di stampa.
// Se non è avvenuta alcuna stampa, questi campi visualizzeranno "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo PRINTDATE
// può visualizzare la data e l'ora dell'ultima operazione di stampa.
// 1 -  Calendario lunare islamico:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Calendario Umm al-Qura:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Calendario nazionale indiano:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Vedi anche

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
