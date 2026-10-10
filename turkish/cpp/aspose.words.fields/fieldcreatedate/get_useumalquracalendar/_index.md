---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar metodu"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar metodu. C++'ta Um‑al‑Qura takvimini kullanıp kullanmayacağını alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldcreatedate/get_useumalquracalendar/
---
## FieldCreateDate::get_UseUmAlQuraCalendar method


Um-al-Qura takvimini kullanıp kullanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar() override
```


## Örnekler



CREATEDATE alanını belgenin oluşturulma tarih/saatini göstermek için nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Belgenin oluşturulma tarih ve saatini göstermek için CREATEDATE alanını kullanabiliriz.
// Aşağıda, CREATEDATE alanının tarih/saat gösterebileceği üç farklı takvim türü bulunmaktadır.
// 1 -  İslami Ay Takvimi:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura takvimi:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Hint Ulusal Takvimi:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Ayrıca Bakınız

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
