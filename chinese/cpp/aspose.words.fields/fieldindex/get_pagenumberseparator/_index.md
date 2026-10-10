---
title: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator 方法"
linktitle: "get_PageNumberSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator 方法。获取或设置在 C++ 中用于分隔索引条目及其页码的字符序列。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.fields/fieldindex/get_pagenumberseparator/
---
## FieldIndex::get_PageNumberSeparator method


获取或设置用于分隔索引条目及其页码的字符序列。

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator()
```


## 示例



展示如何在 INDEX 字段中编辑页码分隔符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// INDEX 条目将把 Text 属性值匹配的 XE 字段分组。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// 如果我们的 INDEX 字段有一组 XE 字段的条目，
// 该条目将显示包含属于此组的 XE 字段的每一页的页码。
// 我们可以设置自定义分隔符来定制这些页码的显示方式。
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// 在插入这些 XE 字段后，INDEX 字段将显示 "First entry, on page(s) 2 & 3 & 4"。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## 另见

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
