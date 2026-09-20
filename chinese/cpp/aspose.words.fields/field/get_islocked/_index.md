---
title: "Aspose::Words::Fields::Field::get_IsLocked 方法"
linktitle: "get_IsLocked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::get_IsLocked 方法。获取或设置字段是否被锁定（不应重新计算其结果），在 C++ 中。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


获取或设置字段是否被锁定（不应重新计算其结果）。

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
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

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
