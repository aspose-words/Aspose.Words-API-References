---
title: "Método Aspose::Words::Node::NodeTypeToString"
linktitle: "NodeTypeToString"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::NodeTypeToString. Un método utilitario que convierte un valor enum de tipo de nodo en una cadena amigable para el usuario en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
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

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
