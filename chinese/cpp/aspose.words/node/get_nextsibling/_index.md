---
title: "Aspose::Words::Node::get_NextSibling method"
linktitle: "get_NextSibling"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::get_NextSibling method. 在 C++ 中获取紧邻此节点之后的节点。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


获取紧随此节点之后的节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
