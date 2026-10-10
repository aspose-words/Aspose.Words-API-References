---
title: "Aspose::Words::Notes::FootnoteType 枚举"
linktitle: "FootnoteType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteType 枚举。指定此项在 C++ 中是脚注还是尾注。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


指定这是脚注还是尾注。

```cpp
enum class FootnoteType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 脚注 | 0 | 该对象是脚注。 |
| 尾注 | 1 | 该对象是一个尾注。 |

## 备注


脚注和尾注都由 [Footnote](./) 类的对象表示。使用 [FootnoteType](../footnote/get_footnotetype/) 来区分脚注和尾注。

## 示例



展示如何使用脚注和尾注引用文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些文本，并使用脚注标记，默认将 IsAuto 属性设置为 "true"，
// 因此正文中看到的标记将自动编号为 "1"，
// 并且脚注将出现在页面底部。
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// 插入更多文本，并使用自定义引用标记的尾注进行标记，
// 该标记将代替数字 "2" 使用，并将 "IsAuto" 设置为 false。
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// 脚注始终出现在其引用文本的底部，
// 因此此分页符不会影响脚注。
// 另一方面，尾注始终位于文档的末尾
// 因此此分页符会将尾注推到下一页。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

## 另见

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
