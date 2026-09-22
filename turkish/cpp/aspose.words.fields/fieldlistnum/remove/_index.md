---
title: "Aspose::Words::Fields::FieldListNum::Remove yöntemi"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldListNum::Remove method. Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, C++'ta null döndürür."
type: docs
weight: 7500
url: /tr/cpp/aspose.words.fields/fieldlistnum/remove/
---
## FieldListNum::Remove method


Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::FieldListNum::Remove() override
```


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

* Class [Node](../../../aspose.words/node/)
* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
