---
title: "Aspose::Words::Story::AppendParagraph 方法"
linktitle: "AppendParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Story::AppendParagraph 方法。一个快捷方法，用于创建带可选文本的 Paragraph 对象并将其追加到此对象的末尾（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/story/appendparagraph/
---
## Story::AppendParagraph method


一个快捷方法，用于创建带可选文本的 [Paragraph](../../paragraph/) 对象并将其追加到此对象的末尾。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::AppendParagraph(const System::String &text)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文本 | const System::String\& | 段落的文本。可以是 **null** 或空字符串。 |

### ReturnValue

新创建并已追加的段落。

## 示例



展示如何创建页眉和页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个页眉并向其追加一个段落。该段落中的文本
// 将出现在此节每页的顶部，位于正文文本之上。
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// 创建一个页脚并向其追加一个段落。该段落中的文本
// 将出现在此节每页的底部，位于正文文本之下。
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## 另见

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
