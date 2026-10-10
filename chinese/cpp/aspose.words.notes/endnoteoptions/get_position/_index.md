---
title: "Aspose::Words::Notes::EndnoteOptions::get_Position 方法"
linktitle: "get_Position"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::EndnoteOptions::get_Position 方法。指定 C++ 中尾注的位置。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.notes/endnoteoptions/get_position/
---
## EndnoteOptions::get_Position method


指定尾注的位置。

```cpp
Aspose::Words::Notes::EndnotePosition Aspose::Words::Notes::EndnoteOptions::get_Position()
```


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

## 另见

* Enum [EndnotePosition](../../endnoteposition/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
