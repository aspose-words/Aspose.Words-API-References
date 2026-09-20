---
title: "Aspose::Words::Document::get_FootnoteOptions 方法"
linktitle: "get_FootnoteOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_FootnoteOptions 方法。提供控制此文档中脚注编号和位置的选项（在 C++ 中）。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words/document/get_footnoteoptions/
---
## Document::get_FootnoteOptions method


提供控制本文件中脚注编号和位置的选项。

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::Document::get_FootnoteOptions()
```


## 示例



展示如何选择文档收集并显示脚注的不同位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 脚注是一种将参考或旁注附加到文本的方式
// 且不会干扰正文文本的流畅性。
// 插入脚注会添加一个小的上标参考符号
// 在我们插入脚注的正文文本中。
// 每个脚注还会在页面底部创建一个条目，该条目由一个符号组成
// 该符号与正文中的引用符号相匹配。
// 我们传递给文档生成器的 "InsertFootnote" 方法的参考文本。
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// 我们可以使用 "Position" 属性来确定文档将在何处放置所有脚注。
// 如果我们将 "Position" 属性的值设置为 "FootnotePosition.BottomOfPage"，
// 每个脚注都会显示在包含其参考标记的页面底部。这是默认值。
// 如果我们将 "Position" 属性的值设置为 "FootnotePosition.BeneathText"，
// 每个脚注都会显示在包含其参考标记的页面文本的末尾。
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```


展示如何更改脚注/尾注参考标记的数字样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 脚注和尾注是一种将参考或旁注附加到文本的方式
// 且不会干扰正文文本的流畅性。
// 插入脚注/尾注会添加一个小的上标参考符号
// 在我们插入脚注/尾注的正文文本中。
// 每个脚注/尾注还会创建一个条目，该条目由与参考符号匹配的符号组成
// 正文文本中的符号。我们传递给文档生成器的 "InsertEndnote" 方法的参考文本。
// 默认情况下，脚注条目显示在包含它们的每页底部
// 它们的参考符号，而尾注显示在文档的末尾。
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// 默认情况下，每个脚注和尾注的参考符号是它们的索引
// 在文档的所有脚注/尾注中。每个文档维护独立的计数
// 分别用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
// 而尾注使用小写罗马数字显示其编号。
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// 我们可以使用 "NumberStyle" 属性为脚注和尾注应用自定义编号样式。
// 这不会影响具有自定义参考标记的脚注/尾注。
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


展示如何在文档的特定位置重新开始脚注/尾注的编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 脚注和尾注是一种将参考或旁注附加到文本的方式
// 且不会干扰正文文本的流畅性。
// 插入脚注/尾注会添加一个小的上标参考符号
// 在我们插入脚注/尾注的正文文本中。
// 每个脚注/尾注还会创建一个条目，该条目由与参考符号匹配的符号组成
// 正文文本中的符号。我们传递给文档生成器的 "InsertEndnote" 方法的参考文本。
// 默认情况下，脚注条目显示在包含它们的每页底部
// 它们的参考符号，而尾注显示在文档的末尾。
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// 默认情况下，每个脚注和尾注的参考符号是它们的索引
// 在文档的所有脚注/尾注中。每个文档维护独立的计数
// 用于脚注和尾注，且在任何情况下都不会重新计数。
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// 我们可以使用 \"RestartRule\" 属性让文档重新计数
// 在新页面或章节时，脚注/尾注计数重新开始。
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


展示如何设置文档开始脚注/尾注计数的数字。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 脚注和尾注是一种将参考或旁注附加到文本的方式
// 且不会干扰正文文本的流畅性。
// 插入脚注/尾注会添加一个小的上标参考符号
// 在我们插入脚注/尾注的正文文本中。
// 每个脚注/尾注还会创建一个条目，该条目由符号组成
// 该符号与正文中的引用符号相匹配。
// 我们传递给文档生成器的 "InsertEndnote" 方法的引用文本。
// 默认情况下，脚注条目显示在包含它们的每页底部
// 它们的参考符号，而尾注显示在文档的末尾。
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// 默认情况下，每个脚注和尾注的参考符号是它们的索引
// 在文档的所有脚注/尾注中。每个文档维护独立的计数
// 用于脚注和尾注，二者均从 1 开始。
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// 我们可以使用 \"StartNumber\" 属性让文档
// 在不同的数字上开始脚注或尾注计数。
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## 另见

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
