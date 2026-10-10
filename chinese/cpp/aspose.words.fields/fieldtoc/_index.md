---
title: "Aspose::Words::Fields::FieldToc 类"
linktitle: "FieldToc"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldToc 类。实现 TOC 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 105000
url: /zh/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


实现 TOC 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | 获取标记用于构建表格的文档部分的书签名称。 |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | 获取或设置在构建不包含标题标签和编号的图表目录时使用的序列标识符名称。 |
| [get_CustomStyles](./get_customstyles/)() | 获取除内置标题样式之外的要包含在目录中的样式列表。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_EntryIdentifier](./get_entryidentifier/)() | 获取应匹配所包含 TC 字段类型标识符的字符串。 |
| [get_EntryLevelRange](./get_entrylevelrange/)() | 获取要包含的目录条目级别范围。 |
| [get_EntrySeparator](./get_entryseparator/)() | 获取分隔条目及其页码的字符序列。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | 获取要包含的标题级别范围。 |
| [get_HideInWebLayout](./get_hideinweblayout/)() | 获取是否在 Web 布局视图中隐藏制表符引导线和页码。 |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | 获取是否将目录条目设为超链接。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | 获取要从中省略页码的目录条目级别范围。 |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | 获取或设置应在条目页码前添加前缀的序列标识符。 |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | 获取是否在表格条目中保留换行符。 |
| [get_PreserveTabs](./get_preservetabs/)() | 获取是否在表格条目中保留制表符。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SequenceSeparator](./get_sequenceseparator/)() | 获取或设置用于分隔序号和页码的字符序列。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | 获取或设置构建图表目录时使用的序列标识符名称。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | 获取是否使用已应用的段落大纲级别。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 设置标记用于构建表格的文档部分的书签名称。 |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/) 的设置器。 |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | 设置除内置标题样式之外的样式列表，以包含在目录中。 |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | 设置一个字符串，以匹配被包含的 TC 字段的类型标识符。 |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | 设置要包含的目录条目级别范围。 |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | 设置用于分隔条目和页码的字符序列。 |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | 设置要包含的标题级别范围。 |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | 设置是否在网页布局视图中隐藏制表符前导和页码。 |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | 设置是否将目录条目设为超链接。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | 设置要从中省略页码的目录条目级别范围。 |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/) 的设置器。 |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | 设置是否在表格条目中保留换行符。 |
| [set_PreserveTabs](./set_preservetabs/)(bool) | 设置是否在表格条目中保留制表符。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/) 的设置器。 |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/) 的设置器。 |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | 设置是否使用已应用的段落大纲级别。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [UpdatePageNumbers](./updatepagenumbers/)() | 更新此目录中项目的页码。 |

## 示例



展示如何使用 SEQ 字段为 TOC 字段填充条目。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOC 字段可以为文档中找到的每个 SEQ 字段在其目录中创建一个条目。
// 每个条目包含包含 SEQ 字段的段落以及该字段所在页的页码。
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// SEQ 字段显示一个在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护独立的计数
// 由 SEQ 字段的 "SequenceIdentifier" 属性标识。
// 使用 "TableOfFiguresLabel" 属性为 TOC 命名主序列。
// 现在，此 TOC 将仅为其 "SequenceIdentifier" 设置为 "MySequence" 的 SEQ 字段创建条目。
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// 我们可以在 "PrefixedSequenceIdentifier" 属性中为另一个 SEQ 字段序列命名。
// 来自此前缀序列的 SEQ 字段不会创建 TOC 条目。
// 每个 TOC 条目从主序列 SEQ 字段创建，现在还会显示计数
// 该计数是前缀序列在生成该条目的主序列 SEQ 字段时的当前值。
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// 每个 TOC 条目将在页面号码左侧立即显示前缀序列计数
// 位于主序列 SEQ 字段出现的页码左侧。
// 我们可以指定一个自定义分隔符，以出现在这两个数字之间。
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 使用 SEQ 字段填充此 TOC 有两种方法。
// 1 -  插入属于 TOC 前缀序列的 SEQ 字段：
// 此字段将把 "PrefixSequence" 的 SEQ 序列计数递增 1。
// 由于此字段不属于已识别的主序列
// 由 TOC 的 "TableOfFiguresLabel" 属性决定，它将不会作为条目出现。
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 - 插入一个属于 TOC 主序列的 SEQ 字段：
// 此 SEQ 字段将在 TOC 中创建一个条目。
// TOC 条目将包含 SEQ 字段所在的段落以及其出现的页码。
// 此条目还将显示前缀序列当前的计数，
// 该计数与页码之间由 TOC 的 SeqenceSeparator 属性值分隔。
// "PrefixSequence" 的计数为 1，此主序列 SEQ 字段位于第 2 页，
// 分隔符为 ">"，因此条目将显示为 "1>2"。
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// 插入一页，将前缀序列递增 2，然后插入 SEQ 字段以随后创建 TOC 条目。
// 前缀序列现在为 2，主序列 SEQ 字段位于第 3 页，
// 因此 TOC 条目将在页码处显示 "2>3"。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
