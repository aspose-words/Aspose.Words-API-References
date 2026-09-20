---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar метод"
linktitle: "get_UseSakaEraCalendar"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar метод. Получает или задает, использовать ли календарь Сака Эра в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldprintdate/get_usesakaeracalendar/
---
## FieldPrintDate::get_UseSakaEraCalendar method


Получает или задает, использовать ли календарь Saka Era.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar() override
```


## Примеры



Показывает прочитанные поля PRINTDATE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Когда документ печатается принтером или печатается как PDF (но не экспортируется в PDF),
// Поля PRINTDATE будут отображать дату/время операции печати.
// Если печать не происходила, эти поля отобразят "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Ниже представлены три разных типа календарей, в соответствии с которыми поле PRINTDATE
// может отображать дату и время последней операции печати.
// 1 -  Исламский лунный календарь:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Календарь Umm al-Qura:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Индийский национальный календарь:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## См. также

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
