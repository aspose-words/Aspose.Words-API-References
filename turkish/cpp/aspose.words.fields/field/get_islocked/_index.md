---
title: "Aspose::Words::Fields::Field::get_IsLocked method"
linktitle: "get_IsLocked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_IsLocked yöntemi. C++'da alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplamamalı)."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
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

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
