---
title: "Aspose::Words::Node::NodeTypeToString Methode"
linktitle: "NodeTypeToString"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::NodeTypeToString Methode. Eine Hilfsmethode, die einen Aufzählungswert des Knotentyps in einen benutzerfreundlichen String in C++ umwandelt."
type: docs
weight: 1000
url: /de/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
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

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
