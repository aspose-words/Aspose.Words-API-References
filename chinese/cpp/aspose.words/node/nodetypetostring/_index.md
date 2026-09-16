---
title: "Aspose::Words::Node::NodeTypeToString 方法"
linktitle: "NodeTypeToString"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::NodeTypeToString 方法。一个实用方法，可将节点类型枚举值转换为 C++ 中的用户友好字符串。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


一个将节点类型枚举值转换为用户友好字符串的实用方法。

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## 示例



展示如何使用节点的 NextSibling 属性遍历其直接子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## 另见

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
