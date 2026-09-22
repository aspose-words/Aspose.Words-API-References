---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar yöntemi"
linktitle: "get_UseLunarCalendar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar yöntemi. C++'ta Hicri Lunar veya İbrani Lunar takvimini kullanıp kullanmayacağını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldprintdate/get_uselunarcalendar/
---
## FieldPrintDate::get_UseLunarCalendar method


Hijri Ay takvimi veya İbrani Ay takvimini kullanıp kullanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar() override
```


## Örnekler



Okunan PRINTDATE alanlarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Bir belge bir yazıcıyla yazdırıldığında veya PDF olarak yazdırıldığında (ancak PDF olarak dışa aktarılmadığında),
// PRINTDATE alanları yazdırma işleminin tarih/saatini gösterecektir.
// Yazdırma gerçekleşmemişse, bu alanlar "0/0/0000" gösterecektir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Aşağıda PRINTDATE alanının göreli olarak kullanabileceği üç farklı takvim türü bulunmaktadır
// son yazdırma işleminin tarih ve saatini gösterebilir.
// 1 -  İslami Ay Takvimi:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura takvimi:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Hint Ulusal Takvimi:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Ayrıca Bakınız

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
