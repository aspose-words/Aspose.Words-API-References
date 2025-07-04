---
title: Aspose::Words::Node::NodeTypeToString method
linktitle: NodeTypeToString
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::NodeTypeToString method. A utility method that converts a node type enum value into a user friendly string in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


A utility method that converts a node type enum value into a user friendly string.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## Examples



Shows how to use a node's NextSibling property to enumerate through its immediate children. 
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

## See Also

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
