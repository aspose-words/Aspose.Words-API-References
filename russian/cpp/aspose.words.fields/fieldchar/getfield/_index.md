---
title: "Aspose::Words::Fields::FieldChar::GetField метод"
linktitle: "GetField"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldChar::GetField. Возвращает поле для символа поля в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fields/fieldchar/getfield/
---
## FieldChar::GetField method


Возвращает поле для символа поля.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldChar::GetField()
```


### ReturnValue

Поле для символа поля.

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

* Class [Field](../../field/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
