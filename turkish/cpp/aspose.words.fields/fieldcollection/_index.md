---
title: "Aspose::Words::Fields::FieldCollection sınıfı"
linktitle: "FieldCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldCollection sınıfı. Belirtilen aralıktaki alanları temsil eden Field nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Belirtilen aralıktaki alanları temsil eden [Field](../field/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) belge makalesini ziyaret edin.

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Bu koleksiyondaki tüm alanları belgelerden ve koleksiyondan kendisinden kaldırır. |
| [get_Count](./get_count/)() | Koleksiyondaki alanların sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir alanı döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Belirtilen alanı bu koleksiyondan ve belgelerden kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir alanı bu koleksiyondan ve belgelerden kaldırır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu koleksiyonun bir örneği, belirtilen aralık içinde başlayan alanları yineleyebilir.

[FieldCollection](./) koleksiyonu, içerdiği alanların sahibi değildir; sadece bir alan seçkisidir.

[FieldCollection](./) koleksiyonu "canlı"dır, yani oluşturulduğu düğüm nesnesinin çocuklarındaki değişiklikler, [FieldCollection](./) özellikleri ve yöntemleri tarafından döndürülen alanlara anında yansır.

## Örnekler



Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Aşağıda bir alan koleksiyonundan alanları kaldırmanın dört yolu verilmiştir.
// 1 -  Kendini kaldıracak bir alan alın:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Kaldırma yöntemine gönderdiğimiz bir alanı kaldırmak için koleksiyonu alın:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Bir indeksteki alanı koleksiyondan kaldırın:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Tüm alanları koleksiyondan bir kerede kaldırın:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
