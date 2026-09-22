---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar metodu"
linktitle: "get_UseLunarCalendar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar metodu. Hijri Lunar veya Hebrew Lunar takvimini C++'de kullanıp kullanmayacağını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldsavedate/get_uselunarcalendar/
---
## FieldSaveDate::get_UseLunarCalendar method


Hijri Ay takvimi veya İbrani Ay takvimini kullanıp kullanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar() override
```


## Örnekler



Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Belgedeki son kaydetme işleminin tarih ve saatini göstermek için SAVEDATE alanını kullanabiliriz.
// Bu alanların referans aldığı kaydetme işlemi, Microsoft Word gibi bir uygulamadaki manuel kaydetmedir,
// belgenin Save metodundan değildir.
// Aşağıda, SAVEDATE alanının tarih/saat görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 -  İslami Ay Takvimi:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura takvimi:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - Hint Ulusal takvimi:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// SAVEDATE alanları tarih/saat değerlerini LastSavedTime yerleşik özelliğinden alır.
// Belgenin Save metodu bu değeri güncellemez, ancak yine de manuel olarak güncelleyebiliriz.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Ayrıca Bakınız

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
