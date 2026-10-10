---
title: "Aspose::Words::Node::get_ParentNode 方法"
linktitle: "get_ParentNode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::get_ParentNode 方法。获取此节点在 C++ 中的直接父节点。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


获取此节点的直接父节点。

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## 备注


如果节点刚刚创建且尚未添加到树中，或已从树中移除，则其父节点为 **null**。

## 示例



展示如何访问节点的父节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 在文档的第一个段落中追加一个子 Run 节点。
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// 该段落是 Run 节点的父节点。我们可以追溯这条血统
// 一直追溯到文档节点，它是文档节点树的根。
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


展示如何创建节点并设置其所属文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 我们尚未将此段落作为子节点追加到任何复合节点。
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// 如果一个节点是另一个复合节点的适当子节点类型，
// 只有当两个节点具有相同的拥有文档时，我们才能将其作为子节点附加。
// 拥有文档是我们传递给节点构造函数的文档。
// 我们尚未将此段落附加到文档中，因此文档不包含其文本。
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// 由于文档拥有此段落，我们可以将其样式之一应用于段落的内容。
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// 将此节点添加到文档中，然后验证其内容。
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
