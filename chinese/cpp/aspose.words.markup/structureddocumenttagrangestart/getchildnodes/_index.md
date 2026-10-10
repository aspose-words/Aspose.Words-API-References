---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes 方法"
linktitle: "GetChildNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes 方法。返回一个实时集合，其中包含匹配指定类型的子节点（C++）。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


返回一个实时集合，包含匹配指定类型的子节点。

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## 示例



展示如何获取 [StructuredDocumentTagRangeStart](../) 的子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Child nodes count: {0}\n", tag->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count()) << std::endl;

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Any, false)))
{
    std::cout << System::String::Format(u"\t|Child node type: {0}", node->get_NodeType()) << std::endl;
}

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    std::cout << System::String::Format(u"\t|Child node text: {0}", node->GetText()) << std::endl;
}
```

## 另见

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
