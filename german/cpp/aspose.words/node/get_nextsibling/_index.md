---
title: "Aspose::Words::Node::get_NextSibling-Methode"
linktitle: "get_NextSibling"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_NextSibling Methode. Gibt den Knoten zurück, der diesem Knoten in C++ unmittelbar folgt."
type: docs
weight: 8000
url: /de/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Ermittelt den Knoten, der diesem Knoten unmittelbar folgt.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
```


## Beispiele



Zeigt, wie die NextSibling‑Eigenschaft eines Knotens verwendet wird, um seine unmittelbaren Kinder zu enumerieren.
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

## Siehe auch

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
