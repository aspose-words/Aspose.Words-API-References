---
title: "Aspose::Words::Node::get_NextSibling metod"
linktitle: "get_NextSibling"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::get_NextSibling metod. Hämtar noden som omedelbart följer denna nod i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Hämtar noden som omedelbart följer denna nod.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
