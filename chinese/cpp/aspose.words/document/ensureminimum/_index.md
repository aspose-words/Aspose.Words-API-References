---
title: "Aspose::Words::Document::EnsureMinimum 方法"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::EnsureMinimum 方法。如果文档不包含任何节，则在 C++ 中创建一个包含一个段落的节。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


如果文档不包含任何节，则创建一个包含一个段落的节。

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## 示例



展示如何确保文档包含编辑其内容所需的最小节点集。
```cpp
// 新创建的文档包含一个子节，该节包括一个子正文和一个子段落。
// 我们可以通过向该段落添加诸如 Run 或内联 Shape 等节点来编辑文档正文的内容。
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// 这是我们编辑文档所需的最小节点集。
// 如果我们删除其中任何一个节点，将无法再编辑文档。
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 调用此方法以确保文档至少拥有这三个节点，从而能够再次编辑它。
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
