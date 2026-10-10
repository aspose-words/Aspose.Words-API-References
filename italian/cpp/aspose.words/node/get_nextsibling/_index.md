---
title: "Metodo Aspose::Words::Node::get_NextSibling"
linktitle: "get_NextSibling"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::get_NextSibling. Ottiene il nodo immediatamente successivo a questo nodo in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Ottiene il nodo immediatamente successivo a questo nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
