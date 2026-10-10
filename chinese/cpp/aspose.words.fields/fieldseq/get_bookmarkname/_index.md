---
title: "Aspose::Words::Fields::FieldSeq::get_BookmarkName 方法"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSeq::get_BookmarkName 方法。获取或设置文档中指向其他位置项的书签名称，而不是当前所在位置（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


获取或设置指向文档中其他位置而非当前位置信息的书签名称。

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## 示例



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

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
