---
title: "Aspose::Words::Fields::Field::get_IsLocked метод"
linktitle: "get_IsLocked"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field::get_IsLocked метод. Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат) в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат).

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
```


## Примеры



Показывает, как работать с узлом [FieldStart](../../fieldstart/).
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

// Получите объект фасада, представляющий поле в документе.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Обновите поле, чтобы отобразить текущую дату.
field->Update();
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
