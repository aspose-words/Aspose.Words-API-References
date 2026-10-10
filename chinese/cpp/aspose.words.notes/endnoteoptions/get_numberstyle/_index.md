---
title: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle 方法"
linktitle: "get_NumberStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle 方法。指定在 C++ 中自动编号的尾注的数字格式。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.notes/endnoteoptions/get_numberstyle/
---
## EndnoteOptions::get_NumberStyle method


指定自动编号尾注的数字格式。

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::EndnoteOptions::get_NumberStyle() override
```

## 备注


并非所有数字样式都适用于此属性。有关适用数字样式的列表，请参阅 Microsoft Word 中的“插入 [Footnote](../../footnote/) 或 Endnote”对话框。如果选择了不适用的数字样式，Microsoft Word 将恢复为默认值。

## 示例



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

## 另见

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
