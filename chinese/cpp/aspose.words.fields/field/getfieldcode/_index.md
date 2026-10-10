---
title: "Aspose::Words::Fields::Field::GetFieldCode 方法"
linktitle: "GetFieldCode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::GetFieldCode 方法。返回字段起始标记和字段分隔符之间的文本（如果没有分隔符，则返回字段结束标记之间的文本）。在 C++ 中，包含子字段的字段代码和字段结果。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## 示例



展示如何使用字段代码向文档插入字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// 此 InsertField 方法的重载会自动更新插入的字段。
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


展示如何获取字段的字段代码。
```cpp
// 打开一个包含在 IF 字段内部的 MERGEFIELD 的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// 获取字段代码有两种方式：
// 1 - 省略其内部字段：
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 - 包含其内部字段：
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// 默认情况下，GetFieldCode 方法显示内部字段。
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** 如果应包含子字段代码。 |

## 示例



展示如何获取字段的字段代码。
```cpp
// 打开一个包含在 IF 字段内部的 MERGEFIELD 的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// 获取字段代码有两种方式：
// 1 - 省略其内部字段：
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 - 包含其内部字段：
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// 默认情况下，GetFieldCode 方法显示内部字段。
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
