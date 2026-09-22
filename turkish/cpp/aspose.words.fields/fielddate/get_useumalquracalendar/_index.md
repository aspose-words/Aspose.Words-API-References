---
title: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar yöntemi"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar yöntemi. C++'ta Um‑al‑Qura takvimini kullanıp kullanmayacağını alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fielddate/get_useumalquracalendar/
---
## FieldDate::get_UseUmAlQuraCalendar method


Um-al-Qura takvimini kullanıp kullanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar() override
```


## Örnekler



DATE alanlarını farklı takvim türlerine göre tarihleri göstermek için nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki metnin her zaman doğru tarihi göstermesini istiyorsak, bir DATE alanı kullanabiliriz.
// Aşağıda, bir DATE alanının bir tarihi göstermek için kullanabileceği üç kültürel takvim türü bulunmaktadır.
// 1 -  İslami Ay Takvimi:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura takvimi:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Hint Ulusal Takvimi:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Bir DATE alanı ekleyin ve takvim türünü, ana uygulama tarafından son kullanılanına ayarlayın.
// Microsoft Word'de, tür Insert -> Text -> Date and Time iletişim kutusunda en son kullanılan olacaktır.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Ayrıca Bakınız

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
