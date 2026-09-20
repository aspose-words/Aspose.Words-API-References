---
title: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator 方法"
linktitle: "get_SequenceSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator 方法。获取或设置用于在 C++ 中分隔序号和页码的字符序列。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.fields/fieldtoc/get_sequenceseparator/
---
## FieldToc::get_SequenceSeparator method


获取或设置用于分隔序号和页码的字符序列。

```cpp
System::String Aspose::Words::Fields::FieldToc::get_SequenceSeparator()
```


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

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
