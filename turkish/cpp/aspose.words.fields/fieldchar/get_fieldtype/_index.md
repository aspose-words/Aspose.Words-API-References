---
title: "Aspose::Words::Fields::FieldChar::get_FieldType yöntemi"
linktitle: "get_FieldType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldChar::get_FieldType yöntemi. C++'de alanın tipini döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


Alan tipini döndürür.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```


## Örnekler



Bir [FieldStart](../../fieldstart/) düğümüyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Belge içindeki alanı temsil eden facade nesnesini alın.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Alanı güncel tarihi gösterecek şekilde güncelleyin.
field->Update();
```

## Ayrıca Bakınız

* Enum [FieldType](../../fieldtype/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
