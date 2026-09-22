---
title: "Aspose::Words::Fields::FieldChar::get_IsDirty yöntemi"
linktitle: "get_IsDirty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldChar::get_IsDirty yöntemi. C++'de belgeye yapılan diğer değişiklikler nedeniyle alanın mevcut sonucunun artık doğru olup olmadığını (eski) alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldchar/get_isdirty/
---
## FieldChar::get_IsDirty method


Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsDirty() const
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

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
