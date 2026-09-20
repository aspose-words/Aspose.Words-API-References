---
title: "Aspose::Words::Range::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Range::NormalizeFieldTypes. Изменяет значения типа поля FieldType у FieldStart, FieldSeparator, FieldEnd в этом диапазоне так, чтобы они соответствовали типам полей, содержащимся в кодах полей в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/range/normalizefieldtypes/
---
## Range::NormalizeFieldTypes method


Изменяет значения типа поля [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) у [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) в этом диапазоне так, чтобы они соответствовали типам полей, содержащимся в кодах полей.

```cpp
void Aspose::Words::Range::NormalizeFieldTypes()
```

## Примечания


Используйте этот метод после изменений документа, влияющих на типы полей.

Чтобы изменить значения типа поля во всём документе, используйте [NormalizeFieldTypes](../../document/normalizefieldtypes/).

## Примеры



Показывает, как поддерживать тип поля в актуальном состоянии с его кодом поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words автоматически определяет типы полей на основе кодов полей.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Вручную измените необработанный текст поля, который определяет код поля.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Изменение кода поля изменило это поле на тип другого типа,
// но свойства типа поля всё ещё отображают старый тип.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Обновите эти свойства с помощью этого метода, чтобы отобразить текущее значение.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
