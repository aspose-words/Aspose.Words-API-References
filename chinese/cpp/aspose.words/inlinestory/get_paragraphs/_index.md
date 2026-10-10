---
title: "Aspose::Words::InlineStory::get_Paragraphs 方法"
linktitle: "get_Paragraphs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::InlineStory::get_Paragraphs 方法。获取在 C++ 中作为故事直接子项的段落集合。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/inlinestory/get_paragraphs/
---
## InlineStory::get_Paragraphs method


获取作为故事直接子节点的段落集合。

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::InlineStory::get_Paragraphs() override
```


## 示例



展示如何插入和自定义脚注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加文本，并用脚注引用它。此脚注将在文本后放置一个小的上标引用
// 标记在它引用的文本之后，并在页面底部的正文下方创建一个条目。
// 此条目将包含脚注的引用标记和引用文本，
// 我们将把它传递给文档生成器的 "InsertFootnote" 方法。
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// 如果此属性设置为 "true"，则我们的脚注引用标记
// 将是其在该节所有脚注中的索引。
// 这是第一个脚注，因此引用标记将是 "1"。
ASSERT_TRUE(footnote->get_IsAuto());

// 我们可以将文档生成器移动到脚注内部以编辑其引用文本。
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// 我们可以设置自定义引用标记，脚注将使用该标记而不是其索引号。
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// 将 "IsAuto" 标志设置为 true 的书签仍会显示其真实索引
// 即使之前的书签显示自定义引用标记，此书签的引用标记仍将是 "3"。
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```


展示如何向段落添加评论。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// 在 Microsoft Word 中，我们可以右键单击文档正文中的此评论进行编辑或回复。
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## 另见

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
