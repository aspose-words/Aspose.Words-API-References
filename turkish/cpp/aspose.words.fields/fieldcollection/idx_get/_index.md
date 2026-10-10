---
title: "Aspose::Words::Fields::FieldCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldCollection::idx_get metodu. Belirtilen indeksteki bir alanı C++'ta döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/fieldcollection/idx_get/
---
## FieldCollection::idx_get method


Belirtilen indeksteki bir alanı döndürür.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

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

* Class [Field](../../field/)
* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
