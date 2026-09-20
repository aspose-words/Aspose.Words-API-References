---
title: "Метод Aspose::Words::Fields::Field::GetFieldCode"
linktitle: "GetFieldCode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::Field::GetFieldCode. Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включает как код поля, так и результат дочерних полей в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
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


Показывает, как получить код поля.
```cpp
// Откройте документ, содержащий MERGEFIELD внутри поля IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Существует два способа получения кода поля:
// 1 -  Опустить его вложенные поля:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Включить его вложенные поля:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает вложенные поля.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** если дочерние коды полей должны быть включены. |

## Примеры



Показывает, как получить код поля.
```cpp
// Откройте документ, содержащий MERGEFIELD внутри поля IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Существует два способа получения кода поля:
// 1 -  Опустить его вложенные поля:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Включить его вложенные поля:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает вложенные поля.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
