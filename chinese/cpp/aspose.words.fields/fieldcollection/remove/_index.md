---
title: "Aspose::Words::Fields::FieldCollection::Remove 方法"
linktitle: "Remove"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCollection::Remove 方法。 在 C++ 中从此集合和文档中移除指定的字段。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection::Remove method


从此集合和文档中移除指定的字段。

```cpp
void Aspose::Words::Fields::FieldCollection::Remove(const System::SharedPtr<Aspose::Words::Fields::Field> &field)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 字段 | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | 要移除的字段。 |

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
