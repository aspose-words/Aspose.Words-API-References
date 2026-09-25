---
title: Aspose::Words::CompositeNode::get_FirstChild method
linktitle: get_FirstChild
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::get_FirstChild method. Gets the first child of the node in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/compositenode/get_firstchild/
---
## CompositeNode::get_FirstChild method


Gets the first child of the node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_FirstChild() const
```


## Examples



Shows how to use a node's NextSibling property to enumerate through its immediate children. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Paragraphs.docx"));

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    System::Console::WriteLine();
    System::Console::WriteLine(System::String::Format(u"Node type: {0}", Node::NodeTypeToString(node->get_NodeType())));

    System::String contents = node->GetText().Trim();
    System::Console::WriteLine(contents == System::String::Empty ? System::String(u"This node contains no text") : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim()));
}
```

## See Also

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
