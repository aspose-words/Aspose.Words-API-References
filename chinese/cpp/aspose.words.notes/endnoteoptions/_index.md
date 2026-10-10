---
title: "Aspose::Words::Notes::EndnoteOptions 类"
linktitle: "EndnoteOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::EndnoteOptions 类。表示文档或章节的尾注编号选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class


表示文档或节的尾注编号选项。欲了解更多，请访问 [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/) 文档文章。

```cpp
class EndnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_NumberStyle](./get_numberstyle/)() override | 指定自动编号尾注的数字格式。 |
| [get_Position](./get_position/)() | 指定尾注的位置。 |
| [get_RestartRule](./get_restartrule/)() override | 确定自动编号何时重新开始。 |
| [get_StartNumber](./get_startnumber/)() override | 指定第一个自动编号脚注的起始数字或字符。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | 用于设置 [Aspose::Words::Notes::EndnoteOptions::get_NumberStyle](./get_numberstyle/) 的 setter。 |
| [set_Position](./set_position/)(Aspose::Words::Notes::EndnotePosition) | 用于设置 [Aspose::Words::Notes::EndnoteOptions::get_Position](./get_position/) 的 setter。 |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | 用于设置 [Aspose::Words::Notes::EndnoteOptions::get_RestartRule](./get_restartrule/) 的 setter。 |
| [set_StartNumber](./set_startnumber/)(int32_t) override | 用于设置 [Aspose::Words::Notes::EndnoteOptions::get_StartNumber](./get_startnumber/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何选择文档收集并显示尾注的不同位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 尾注是一种将引用或旁注附加到文本的方法
// 且不会干扰正文文本的流畅性。
// 插入尾注会添加一个小的上标引用符号
// 在我们插入尾注的正文文本处。
// 每个尾注还会在文档末尾创建一个条目，由符号组成
// 该符号与正文中的引用符号相匹配。
// 我们传递给文档生成器的 "InsertEndnote" 方法的引用文本。
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// 我们可以使用 "Position" 属性来确定文档将把所有尾注放置在哪里。
// 如果我们将 "Position" 属性的值设为 "EndnotePosition.EndOfDocument"，
// 每个脚注都会出现在文档末尾的集合中。这是默认值。
// 如果我们将 "Position" 属性的值设为 "EndnotePosition.EndOfSection"，
// 每个脚注都会出现在包含尾注引用标记的章节末尾的集合中。
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
