---
title: "Aspose::Words::HeaderFooter::HeaderFooter 构造函数"
linktitle: "HeaderFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::HeaderFooter::HeaderFooter 构造函数。创建一个指定类型的新页眉或页脚，使用 C++。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


创建指定类型的新页眉或页脚。

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
| headerFooterType | Aspose::Words::HeaderFooterType | 一个指定页眉或页脚类型的 [HeaderFooterType](../get_headerfootertype/) 值。 |
## 备注


当创建 [HeaderFooter](../) 时，它属于指定的文档，但尚未成为文档的一部分，并且 [ParentNode](../../node/get_parentnode/) 为 **null**。

要将 [HeaderFooter](../) 追加到 [Section](../../section/)，请使用 [InsertAfter1()</see>, <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../)，或使用 [HeadersFooters](../../section/get_headersfooters/) 属性和方法 [Add()](../)、[Insert()](../)。

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

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
