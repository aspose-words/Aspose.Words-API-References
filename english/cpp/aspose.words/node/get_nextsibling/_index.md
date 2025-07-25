---
title: Aspose::Words::Node::get_NextSibling method
linktitle: get_NextSibling
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::get_NextSibling method. Gets the node immediately following this node in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Gets the node immediately following this node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
