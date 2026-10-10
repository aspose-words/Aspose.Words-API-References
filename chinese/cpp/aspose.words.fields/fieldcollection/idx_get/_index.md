---
title: "Aspose::Words::Fields::FieldCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCollection::idx_get 方法。 在 C++ 中返回指定索引处的字段。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fields/fieldcollection/idx_get/
---
## FieldCollection::idx_get method


返回指定索引处的字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 集合中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

## 示例



展示如何从字段集合中移除字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// 以下是从字段集合中删除字段的四种方法。
// 1 -  获取字段自行删除：
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  获取集合以删除我们传递给其删除方法的字段：
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  在索引处从集合中删除字段：
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  一次性删除集合中的所有字段：
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## 另见

* Class [Field](../../field/)
* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
