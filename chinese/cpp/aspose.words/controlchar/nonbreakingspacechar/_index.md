---
title: "Aspose::Words::ControlChar::NonBreakingSpaceChar 字段"
linktitle: "NonBreakingSpaceChar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ControlChar::NonBreakingSpaceChar 字段。非换行空格字符：(char)160 在 C++ 中。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words/controlchar/nonbreakingspacechar/
---
## NonBreakingSpaceChar field


不换行空格字符: (char)160。

```cpp
static constexpr char16_t Aspose::Words::ControlChar::NonBreakingSpaceChar
```


## 示例



展示如何向文档添加各种控制字符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加普通空格。
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::SpaceChar + u"After space.");

// 添加 NBSP，即不换行空格。
// 不同于普通空格，此空格在其位置上不能自动换行。
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::NonBreakingSpace() + u"After space.");

// 添加一个制表符。
builder->Write(System::String(u"Before tab.") + Aspose::Words::ControlChar::Tab() + u"After tab.");

// 添加换行符。
builder->Write(System::String(u"Before line break.") + Aspose::Words::ControlChar::LineBreak() + u"After line break.");

// 添加新行并开始一个新段落。
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());
builder->Write(System::String(u"Before line feed.") + Aspose::Words::ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// 换行符有两种形式。
ASSERT_EQ(Aspose::Words::ControlChar::LineFeed(), Aspose::Words::ControlChar::Lf());

// 回车和换行可以用一个字符一起表示。
ASSERT_EQ(Aspose::Words::ControlChar::CrLf(), Aspose::Words::ControlChar::Cr() + Aspose::Words::ControlChar::Lf());

// 添加段落分隔符，这将开始一个新段落。
builder->Write(System::String(u"Before paragraph break.") + Aspose::Words::ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// 添加节分隔符。这不会创建新的节或段落。
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(System::String(u"Before section break.") + Aspose::Words::ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// 添加分页符。
builder->Write(System::String(u"Before page break.") + Aspose::Words::ControlChar::PageBreak() + u"After page break.");

// 分页符的值与节分隔符相同。
ASSERT_EQ(Aspose::Words::ControlChar::PageBreak(), Aspose::Words::ControlChar::SectionBreak());

// 插入一个新节，然后将其列数设置为两列。
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// 我们可以使用控制字符来标记文本移动到下一列的位置。
builder->Write(System::String(u"Text at end of column 1.") + Aspose::Words::ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// 大多数字符都有 char 和 string 对应形式。
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Cell()), Aspose::Words::ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::NonBreakingSpace()), Aspose::Words::ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Tab()), Aspose::Words::ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineBreak()), Aspose::Words::ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineFeed()), Aspose::Words::ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ParagraphBreak()), Aspose::Words::ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::SectionBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::PageBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ColumnBreak()), Aspose::Words::ControlChar::ColumnBreakChar);
```

## 另见

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
