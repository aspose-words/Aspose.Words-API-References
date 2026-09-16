---
title: "Aspose::Words::Fields::FieldSeq 类"
linktitle: "FieldSeq"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSeq 类。实现 SEQ 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 91000
url: /zh/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


实现 SEQ 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | 获取或设置指向文档中其他位置而非当前位置信息的书签名称。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_InsertNextNumber](./get_insertnextnumber/)() | 获取或设置是否为指定项目插入下一个序列号。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | 获取或设置一个整数，表示要将序列号重置到的标题级别。如果该数字不存在，则返回 -1。 |
| [get_ResetNumber](./get_resetnumber/)() | 获取或设置一个整数，以将序列号重置到该值。如果该数字不存在，则返回 -1。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | 获取或设置分配给要编号的项目系列的名称。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 设置器用于 [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/)。 |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | 设置器用于 [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/)。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | 设置器用于 [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/)。 |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | 设置器用于 [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/)。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | 设置器用于 [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

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


展示使用 SEQ 字段创建编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ 字段显示一个在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护独立的计数
// 由 SEQ 字段的 "SequenceIdentifier" 属性标识。
// 插入一个 SEQ 字段，以显示 "MySequence" 的当前计数值，
// 在使用 "ResetNumber" 属性将其设置为 100 之后。
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// 使用另一个 SEQ 字段显示此序列的下一个数字。
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// 插入一级标题。
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// 插入同一序列的另一个 SEQ 字段，并将其配置为在每个标题处将计数重置为 1。
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// 上述标题是一级标题，因此此序列的计数被重置为 1。
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// 移动到此序列的下一个数字。
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


展示如何将目录和序列字段结合使用。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOC 字段可以为文档中找到的每个 SEQ 字段在其目录中创建一个条目。
// 每个条目包含包含 SEQ 字段的段落，
// 以及字段出现的页码。
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// 将此 TOC 字段配置为具有值为 "MySequence" 的 SequenceIdentifier 属性。
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// 将此 TOC 字段配置为仅获取位于书签范围内的 SEQ 字段
// 命名为 "TOCBookmark"。
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// SEQ 字段显示一个在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护独立的计数
// 由 SEQ 字段的 "SequenceIdentifier" 属性标识。
// 插入一个 SEQ 字段，其序列标识符与 TOC 的
// TableOfFiguresLabel 属性。由于它位于外部，此字段不会在 TOC 中创建条目。
// 由 "BookmarkName" 指定的书签范围。
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// 此 SEQ 字段的序列匹配 TOC 的 "TableOfFiguresLabel" 属性，并且位于书签的范围内。
// 包含此字段的段落将在 TOC 中显示为条目。
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// 此 SEQ 字段的序列未匹配 TOC 的 "TableOfFiguresLabel" 属性，
// 但位于书签的范围内。其段落将不会在 TOC 中显示为条目。
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// 此 SEQ 字段的序列匹配 TOC 的 "TableOfFiguresLabel" 属性，并且位于书签的范围内。
// 此字段还引用了另一个书签。该书签的内容将出现在此 SEQ 字段的 TOC 条目中。
// SEQ 字段本身不会显示该书签的内容。
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// 创建一个书签，其内容由于上述 SEQ 字段的引用而会出现在 TOC 条目中。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
