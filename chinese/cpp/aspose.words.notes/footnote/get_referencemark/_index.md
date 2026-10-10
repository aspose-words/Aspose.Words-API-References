---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark 方法"
linktitle: "get_ReferenceMark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark 方法。获取/设置用于此脚注的自定义引用标记。默认值为空字符串，表示在 C++ 中使用自动编号的脚注。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


获取/设置用于此脚注的自定义引用标记。默认值为 **empty string**，表示使用自动编号的脚注。

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## 备注


如果此属性设置为 **empty string** 或 **null**，则 [IsAuto](../get_isauto/) 属性将自动设置为 **true**；如果设置为其他任何值，则 [IsAuto](../get_isauto/) 将被设置为 **false**。

RTF 格式只能将 1 个符号存储为自定义引用标记，因此在导出时仅会写入第一个符号，其他的将被丢弃。

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

## 另见

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
