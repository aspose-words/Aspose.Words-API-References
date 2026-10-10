---
title: "Aspose::Words::Fields::FieldIndex::get_BookmarkName 方法"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex::get_BookmarkName 方法。获取或设置用于标记文档中用于构建索引的部分的书签名称（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldindex/get_bookmarkname/
---
## FieldIndex::get_BookmarkName method


获取或设置书签的名称，该书签标记用于生成索引的文档部分。

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_BookmarkName()
```


## 示例



展示如何创建 INDEX 字段，然后使用 XE 字段填充条目。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值
// 以及包含 XE 字段的页面在右侧。
// 如果 XE 字段在其 "Text" 属性中的值相同，
// INDEX 字段会将它们分组为一个条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// 仅配置 INDEX 字段以显示位于范围内的 XE 字段
// 书签名为 "MainBookmark"，且其 "EntryType" 属性的值为 "A"。
// 对于 INDEX 和 XE 字段，"EntryType" 属性仅使用其字符串值的第一个字符。
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// 在新页面上，使用与该值匹配的名称开始书签
// INDEX 字段的 "BookmarkName" 属性的值。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// INDEX 字段会捕获此条目，因为它位于书签内部，
// 并且它的条目类型也匹配 INDEX 字段的条目类型。
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// 插入一个 XE 字段，由于条目类型不匹配，它不会出现在 INDEX 中。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// 结束书签并随后插入一个 XE 字段。
// 它与 INDEX 字段类型相同，但不会出现
// 因为它位于书签的边界之外。
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## 另见

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
