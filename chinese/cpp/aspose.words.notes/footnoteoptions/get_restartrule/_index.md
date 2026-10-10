---
title: "Aspose::Words::Notes::FootnoteOptions::get_RestartRule 方法"
linktitle: "get_RestartRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteOptions::get_RestartRule 方法。确定在 C++ 中何时重新启动自动编号。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.notes/footnoteoptions/get_restartrule/
---
## FootnoteOptions::get_RestartRule method


确定自动编号何时重新开始。

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::FootnoteOptions::get_RestartRule() override
```


## 示例



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

## 另见

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
