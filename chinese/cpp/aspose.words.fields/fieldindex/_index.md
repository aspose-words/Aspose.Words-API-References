---
title: "Aspose::Words::Fields::FieldIndex 类"
linktitle: "FieldIndex"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex 类。实现 INDEX 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 59000
url: /zh/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


实现 INDEX 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | 获取或设置书签的名称，该书签标记用于生成索引的文档部分。 |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | 获取或设置用于分隔交叉引用和其他条目的字符序列。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_EntryType](./get_entrytype/)() | 获取或设置用于生成索引的索引条目类型。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | 获取一个值，指示是否通过字段代码覆盖页码分隔符。 |
| [get_HasSequenceName](./get_hassequencename/)() | 获取一个值，指示在构建字段结果时是否应使用序列。 |
| [get_Heading](./get_heading/)() | 获取或设置在每个给定字母的条目集合开始处出现的标题。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LanguageId](./get_languageid/)() | 获取或设置用于生成索引的语言 ID。 |
| [get_LetterRange](./get_letterrange/)() | 获取或设置索引限制的字母范围。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_NumberOfColumns](./get_numberofcolumns/)() | 获取或设置构建索引时每页使用的列数。 |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | 获取或设置用于在页码列表中分隔两个页码的字符序列。 |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | 获取或设置用于分隔索引条目及其页码的字符序列。 |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | 获取或设置用于分隔页码范围起止的字符序列。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | 获取或设置是否将子条目放在与主条目同一行。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SequenceName](./get_sequencename/)() | 获取或设置其编号随页码一起包含的序列名称。 |
| [get_SequenceSeparator](./get_sequenceseparator/)() | 获取或设置用于分隔序号和页码的字符序列。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_UseYomi](./get_useyomi/)() | 获取或设置是否启用索引条目的假名文本。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/) 的设置器。 |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/) 的设置器。 |
| [set_EntryType](./set_entrytype/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/) 的设置器。 |
| [set_Heading](./set_heading/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/) 的设置器。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LanguageId](./set_languageid/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/) 的设置器。 |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/) 的设置器。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/)。 |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/)。 |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/)。 |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/)。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | 设置 [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)。 |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/)。 |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | 设置 [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/)。 |
| [set_UseYomi](./set_useyomi/)(bool) | 设置 [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
