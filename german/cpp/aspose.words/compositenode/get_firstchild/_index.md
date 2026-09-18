---
title: "Aspose::Words::CompositeNode::get_FirstChild Methode"
linktitle: "get_FirstChild"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::get_FirstChild Methode. Gibt das erste untergeordnete Element des Knotens in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words/compositenode/get_firstchild/
---
## CompositeNode::get_FirstChild method


Ermittelt das erste Kind des Knotens.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_FirstChild() const
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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
