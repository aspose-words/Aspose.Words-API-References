---
title: "Aspose::Words::Fields::FieldCollection::Clear 方法"
linktitle: "清除"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCollection::Clear 方法。 在 C++ 中，从文档中以及该集合本身中移除此集合的所有字段。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection::Clear method


从文档以及该集合本身中移除此集合的所有字段。

```cpp
void Aspose::Words::Fields::FieldCollection::Clear()
```


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

* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
