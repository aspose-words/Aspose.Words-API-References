---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType 方法"
linktitle: "get_FootnoteType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType 方法。返回一个值，用于指定此项是脚注还是尾注，在 C++ 中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


返回一个值，指定这是脚注还是尾注。

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## 示例



显示脚注和尾注之间的区别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面是将编号引用附加到文本的两种方式。这两个引用都将添加一个
// 小的上标引用标记，在我们插入它们的位置。
// 默认情况下，引用标记是文档中所有引用之间的索引号。
// 每个引用还会创建一个条目，其引用标记与正文中的相同
// 以及引用文本，我们将把它传递给文档生成器的 "InsertFootnote" 方法。
// 1 -  脚注，其条目将出现在引用文本的同一页上：
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  尾注，其条目将出现在文档的末尾：
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## 另见

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
