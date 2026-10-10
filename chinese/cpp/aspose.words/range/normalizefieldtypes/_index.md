---
title: "Aspose::Words::Range::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::NormalizeFieldTypes 方法。更改此范围内 FieldStart、FieldSeparator、FieldEnd 的字段类型值 FieldType，使其对应于 C++ 中字段代码中包含的字段类型。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/range/normalizefieldtypes/
---
## Range::NormalizeFieldTypes method


更改此范围内 [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) 的字段类型值，针对 [FieldStart](../../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../../aspose.words.fields/fieldend/)，使其对应于字段代码中包含的字段类型。

```cpp
void Aspose::Words::Range::NormalizeFieldTypes()
```

## 备注


在影响字段类型的文档更改后使用此方法。

要在整个文档中更改字段类型值，请使用 [NormalizeFieldTypes](../../document/normalizefieldtypes/)。

## 示例



展示如何使字段的类型与其字段代码保持同步。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words 会根据字段代码自动检测字段类型。
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// 手动更改字段的原始文本，该文本决定字段代码。
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// 更改字段代码后，此字段已变为不同类型，
// 但字段的类型属性仍显示旧的类型。
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// 使用此方法更新这些属性，以显示当前值。
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
