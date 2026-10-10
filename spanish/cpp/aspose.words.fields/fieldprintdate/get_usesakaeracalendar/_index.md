---
title: "Método get_UseSakaEraCalendar de Aspose::Words::Fields::FieldPrintDate"
linktitle: "get_UseSakaEraCalendar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_UseSakaEraCalendar de Aspose::Words::Fields::FieldPrintDate. Obtiene o establece si se debe usar el calendario Saka Era en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldprintdate/get_usesakaeracalendar/
---
## FieldPrintDate::get_UseSakaEraCalendar method


Obtiene o establece si se debe usar el calendario de la era Saka.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar() override
```


## Ejemplos



Muestra los campos PRINTDATE leídos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Cuando un documento se imprime en una impresora o se imprime como PDF (pero no se exporta a PDF),
// Los campos PRINTDATE mostrarán la fecha/hora de la operación de impresión.
// Si no se ha realizado ninguna impresión, estos campos mostrarán "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// A continuación se presentan tres tipos de calendario diferentes según los cuales el campo PRINTDATE
// puede mostrar la fecha y hora de la última operación de impresión.
// 1 -  Calendario lunar islámico:
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

// 3 -  Calendario nacional indio:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Ver también

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
