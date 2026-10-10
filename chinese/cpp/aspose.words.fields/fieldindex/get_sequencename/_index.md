---
title: "Aspose::Words::Fields::FieldIndex::get_SequenceName 方法"
linktitle: "get_SequenceName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndex::get_SequenceName 方法。获取或设置序列的名称，该序列的编号会与页码一起包含在 C++ 中。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.fields/fieldindex/get_sequencename/
---
## FieldIndex::get_SequenceName method


获取或设置其编号随页码一起包含的序列名称。

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceName()
```


## 示例



展示如何通过组合 INDEX 和 SEQ 字段将文档拆分为多个部分。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 INDEX 字段，该字段将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 并在右侧显示包含 XE 字段的页码。
// 如果 XE 字段在其 "Text" 属性中的值相同，
// INDEX 字段会将它们分组为一个条目。
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// 在 SequenceName 属性中，为 SEQ 字段序列命名。此 INDEX 字段的每个条目现在还将显示
// 该序列计数在创建此条目的 XE 字段位置上的编号。
index->set_SequenceName(u"MySequence");

// 设置文本，以在序列和页码周围解释其含义给用户。
// 使用此配置创建的条目将在其页码处显示类似 "MySequence at 1 on page 1" 的内容。
// PageNumberSeparator 和 SequenceSeparator 的长度不能超过 15 个字符。
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// SEQ 字段显示一个在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护独立的计数
// 由 SEQ 字段的 "SequenceIdentifier" 属性标识。
// 插入一个 SEQ 字段，将 “MySequence” 序列移动到 1。
// 此字段与普通文档文本没有区别。它不会出现在 INDEX 字段的目录中。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// 插入一个 XE 字段，它将在 INDEX 字段中创建一个条目。
// 由于 “MySequence” 位于 1，且此 XE 字段位于第 2 页，加上我们上面定义的自定义分隔符，
// 此字段的 INDEX 条目将在左侧显示 “Cat”，右侧显示 “MySequence at 1 on page 2”。
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// 插入分页符并使用 SEQ 字段将 “MySequence” 推进到 3。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// 插入一个 XE 字段，其 Text 属性与上述相同。
// INDEX 条目将把 Text 属性值匹配的 XE 字段分组。
// 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
// 由于我们在第 2 页且 “MySequence” 为 3，“, 3 on page 3” 将被追加到上述相同的 INDEX 条目中。
// 该 INDEX 条目的页码部分现在将显示 “MySequence at 1 on page 2, 3 on page 3”。
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// 插入一个具有全新且唯一 Text 属性值的 XE 字段。
// 这将添加一个新条目，显示 MySequence 在第 4 页的 3。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## 另见

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
