---
title: "Aspose::Words::Fields::Field::get_Result метод"
linktitle: "get_Result"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field::get_Result метод. Получает или задает текст, находящийся между разделителем поля и его концом в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Получает или задает текст, находящийся между разделителем поля и его концом.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Примеры



Показывает, как вставить поле в документ, используя код поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
