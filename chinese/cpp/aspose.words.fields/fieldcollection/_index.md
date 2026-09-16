---
title: "Aspose::Words::Fields::FieldCollection 类"
linktitle: "FieldCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCollection 类。一个 Field 对象的集合，表示指定范围内的字段。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


一个 [Field](../field/) 对象的集合，表示指定范围内的字段。要了解更多信息，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 从文档以及该集合本身中移除此集合的所有字段。 |
| [get_Count](./get_count/)() | 返回集合中字段的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的字段。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | 从此集合和文档中移除指定的字段。 |
| [RemoveAt](./removeat/)(int32_t) | 从此集合和文档中移除指定索引处的字段。 |
| static [Type](./type/)() |  |
## 备注


此集合的实例遍历位于指定范围内开始的字段。

该 [FieldCollection](./) 集合并不拥有其包含的字段，而只是字段的一个选择。

该 [FieldCollection](./) 集合是“实时”的，即对其创建来源的节点对象的子节点所做的更改会立即体现在 [FieldCollection](./) 属性和方法返回的字段中。

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
