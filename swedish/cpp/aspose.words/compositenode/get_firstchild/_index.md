---
title: "Aspose::Words::CompositeNode::get_FirstChild metod"
linktitle: "get_FirstChild"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::get_FirstChild metod. Hämtar den första barnnoden i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/compositenode/get_firstchild/
---
## CompositeNode::get_FirstChild method


Hämtar det första barnet till noden.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_FirstChild() const
```


## Exempel



Visar hur man använder en nods NextSibling‑egenskap för att iterera genom dess omedelbara barn.
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

## Se även

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
