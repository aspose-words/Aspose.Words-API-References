---
title: "Aspose::Words::Paragraph::get_ParentStory 方法"
linktitle: "get_ParentStory"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_ParentStory 方法。检索可以是 Body 或 HeaderFooter 的父级节级故事，使用 C++。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words/paragraph/get_parentstory/
---
## Paragraph::get_ParentStory method


检索可以是 [Body](../../body/) 或 [HeaderFooter](../../headerfooter/) 的父级节级故事。

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::Paragraph::get_ParentStory()
```


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

* Class [Story](../../story/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
