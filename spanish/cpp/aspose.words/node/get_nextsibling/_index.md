---
title: "Método Aspose::Words::Node::get_NextSibling"
linktitle: "get_NextSibling"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_NextSibling. Obtiene el nodo que sigue inmediatamente a este nodo en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Obtiene el nodo que sigue inmediatamente a este nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
```


## Ejemplos



Muestra cómo usar la propiedad NextSibling de un nodo para enumerar sus hijos inmediatos.
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

## Ver también

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
