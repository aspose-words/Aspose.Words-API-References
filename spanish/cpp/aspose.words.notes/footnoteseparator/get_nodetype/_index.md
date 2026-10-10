---
title: "Método get_NodeType de Aspose::Words::Notes::FootnoteSeparator"
linktitle: "get_NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_NodeType de Aspose::Words::Notes::FootnoteSeparator. Obtiene el tipo de este nodo en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.notes/footnoteseparator/get_nodetype/
---
## FootnoteSeparator::get_NodeType method


Obtiene el tipo de este nodo.

```cpp
Aspose::Words::NodeType Aspose::Words::Notes::FootnoteSeparator::get_NodeType() const override
```


## Ejemplos



Muestra cómo eliminar todos los nodos hijos de un tipo específico de un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Guarde el nodo hermano siguiente como una variable por si queremos movernos a él después de eliminar este nodo.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Un cuerpo de sección puede contener nodos Paragraph y Table.
    // Si el nodo es una Tabla, elimínalo del nodo padre.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [FootnoteSeparator](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
