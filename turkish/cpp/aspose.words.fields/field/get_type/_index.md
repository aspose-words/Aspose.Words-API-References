---
title: "Aspose::Words::Fields::Field::get_Type metodu"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_Type metodu. C++'ta Microsoft Word alan türünü alır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.fields/field/get_type/
---
## Field::get_Type method


Microsoft Word alan türünü alır.

```cpp
virtual Aspose::Words::Fields::FieldType Aspose::Words::Fields::Field::get_Type() const
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

* Enum [FieldType](../../fieldtype/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
