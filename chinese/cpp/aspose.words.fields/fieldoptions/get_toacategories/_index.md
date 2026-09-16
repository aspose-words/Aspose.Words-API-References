---
title: "Aspose::Words::Fields::FieldOptions::get_ToaCategories 方法"
linktitle: "get_ToaCategories"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_ToaCategories 方法。获取或设置 C++ 中的权限类别表。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_toacategories/
---
## FieldOptions::get_ToaCategories method


获取或设置权威类别表。

```cpp
const System::SharedPtr<Aspose::Words::Fields::ToaCategories> & Aspose::Words::Fields::FieldOptions::get_ToaCategories() const
```


## 示例



展示如何为 TOA 字段指定一组类别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOA 字段可以通过此集合中定义的类别过滤其条目。
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// 此类别集合带有默认值，我们可以用自定义值覆盖它们。
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// 我们始终可以通过此集合访问默认值。
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// 插入 2 个 TOA 字段。TOA 字段会为文档中的每个 TA 字段创建一个条目。
// 使用 "\c" 开关从我们的集合中选择类别的索引。
//  使用此开关，TOA 字段只会获取来自 TA 字段的条目，这些字段
// 也具有匹配类别索引的 "\c" 开关。每个 TOA 字段还会显示
// 其 "\c" 开关指向的类别名称。
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 在 2 个类别中插入 TOA 条目。我们的第一个 TOA 字段将收到一个条目，
// 来自第二个 TA 字段，该字段的 "\c" 开关也指向第一个类别。
// 第二个 TOA 字段将拥有来自另外两个 TA 字段的两个条目。
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## 另见

* Class [ToaCategories](../../toacategories/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
