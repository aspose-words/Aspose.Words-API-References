---
title: "Aspose::Words::Fields::FieldXE::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldXE::get_Text 方法。获取或设置 C++ 中条目的文本。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/fieldxe/get_text/
---
## FieldXE::get_Text method


获取或设置条目的文本。

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Text()
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


展示如何使用 XE 字段填充 INDEX 字段的条目，并修改其外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// 如果 XE 字段在其 "Text" 属性中的值相同，
// INDEX 字段会将它们分组为一个条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// 将此属性的值设为 "A" 将按首字母对所有条目进行分组，
// 并在每组上方放置该大写字母。
index->set_Heading(u"A");

// 将 INDEX 字段创建的表格设置为跨越 2 列。
index->set_NumberOfColumns(u"2");

// 将首字母超出 "a-c" 范围的任何条目设置为省略。
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// 接下来的两个 XE 字段将显示在 "A" 标题下，
// 其各自的文本样式也将应用于页码。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// 接下来的两个 XE 字段将在 INDEX 字段目录中分别位于 "B" 和 "C" 标题下。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// INDEX 字段按字母顺序对所有条目进行排序，因此此条目将与另外两个一起显示在 "A" 下。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// 此条目不会出现，因为它以字母 "D" 开头，
// 这超出了 INDEX 字段的 LetterRange 属性定义的 "a-c" 字符范围。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## 另见

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
