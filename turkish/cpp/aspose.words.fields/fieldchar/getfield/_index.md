---
title: "Aspose::Words::Fields::FieldChar::GetField yöntemi"
linktitle: "GetField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldChar::GetField yöntemi. C++'ta alan karakteri için bir alan döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fieldchar/getfield/
---
## FieldChar::GetField method


Alan karakteri için bir alan döndürür.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldChar::GetField()
```


### ReturnValue

Alan karakteri için bir alan.

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

* Class [Field](../../field/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
