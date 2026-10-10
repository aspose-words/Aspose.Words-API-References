---
title: "Aspose::Words::Fields::Field::get_Result 方法"
linktitle: "get_Result"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::get_Result 方法。获取或设置位于字段分隔符和字段结束之间的文本（在 C++ 中）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


获取或设置位于字段分隔符和字段结束之间的文本。

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
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

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
