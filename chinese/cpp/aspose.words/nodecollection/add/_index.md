---
title: "Aspose::Words::NodeCollection::Add 方法"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::Add 方法。在 C++ 中将节点添加到集合的末尾。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


在集合的末尾添加一个节点。

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 节点 | const System::SharedPtr\<Aspose::Words::Node\>\& | 要添加到集合末尾的节点。 |
## 备注


该节点作为子节点插入到创建集合的节点对象中。

如果要插入的节点是从另一个文档创建的，您应该使用 [ImportNode()](../) 将节点导入到当前文档。导入后的节点随后可以插入到当前文档中。

## 示例



展示如何准备一个新的节节点以进行编辑。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 一个空白文档自带一个节，该节有一个正文，正文中又包含一个段落。
// 我们可以通过向该段落添加文本运行、形状或表格等元素来向此文档添加内容。
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// 如果我们这样添加一个新节，它将没有正文或任何其他子节点。
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 运行 "EnsureMinimum" 方法，为此节添加正文和段落，以开始编辑。
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
