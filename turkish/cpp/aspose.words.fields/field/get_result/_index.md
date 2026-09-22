---
title: "Aspose::Words::Fields::Field::get_Result yöntemi"
linktitle: "get_Result"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_Result yöntemi. C++'ta alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Örnekler



Bir alan kodu kullanarak bir belgeye alan eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
