---
title: "Metodo Aspose::Words::Node::NodeTypeToString"
linktitle: "NodeTypeToString"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::NodeTypeToString. Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## Esempi



Mostra come utilizzare la proprietà NextSibling di un nodo per enumerare i suoi figli immediati.
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

## Vedi anche

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
