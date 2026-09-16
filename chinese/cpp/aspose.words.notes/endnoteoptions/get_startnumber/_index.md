---
title: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber 方法"
linktitle: "get_StartNumber"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber 方法。指定 C++ 中第一个自动编号的尾注的起始数字或字符。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.notes/endnoteoptions/get_startnumber/
---
## EndnoteOptions::get_StartNumber method


指定第一个自动编号脚注的起始数字或字符。

```cpp
int32_t Aspose::Words::Notes::EndnoteOptions::get_StartNumber() override
```

## 备注


此属性仅在将 [RestartRule](../get_restartrule/) 设置为 [Continuous](../../footnotenumberingrule/) 时生效。

## 示例



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

* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
