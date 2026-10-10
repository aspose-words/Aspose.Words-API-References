---
title: "Aspose::Words::Fields::FieldChar::get_FieldType 方法"
linktitle: "get_FieldType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldChar::get_FieldType 方法。返回字段在 C++ 中的类型。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


返回字段的类型。

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```


## 示例



展示如何使用 [FieldStart](../../fieldstart/) 节点。
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

// 检索表示文档中字段的外观对象。
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// 更新字段以显示当前日期。
field->Update();
```

## 另见

* Enum [FieldType](../../fieldtype/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
