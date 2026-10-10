---
title: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator method"
linktitle: "get_PageRangeSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator 方法。获取或设置在 C++ 中用于分隔页范围起止的字符序列。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.fields/fieldindex/get_pagerangeseparator/
---
## FieldIndex::get_PageRangeSeparator method


获取或设置用于分隔页码范围起止的字符序列。

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator()
```


## 示例



展示如何将书签跨越的页面指定为 INDEX 字段条目的页面范围。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// 对于显示页面范围的 INDEX 条目，我们可以指定一个分隔字符串
// 该字符串将出现在第一页的页码和最后一页的页码之间。
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// 如果 XE 字段使用 PageRangeBookmarkName 属性命名书签，
// 其 INDEX 条目将显示书签跨越的页面范围
// 而不是包含 XE 字段的页面的页码。
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// 插入一个书签，起始于第 3 页，结束于第 5 页。
// 引用此书签的 XE 字段的 INDEX 条目将显示此页面范围。
// 在我们的表格中，INDEX 条目将显示 "My entry, on page(s) 3 to 5"。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## 另见

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
