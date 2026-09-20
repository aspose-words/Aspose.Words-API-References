---
title: "Método Aspose::Words::Node::get_CustomNodeId"
linktitle: "get_CustomNodeId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_CustomNodeId. Especifica un identificador de nodo personalizado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/node/get_customnodeid/
---
## Node::get_CustomNodeId method


Especifica un identificador de nodo personalizado.

```cpp
int32_t Aspose::Words::Node::get_CustomNodeId() const
```

## Observaciones


El valor predeterminado es cero.

Este identificador puede establecerse y usarse arbitrariamente. Por ejemplo, como una clave para obtener datos externos.

Nota importante, el valor especificado no se guarda en un archivo de salida y solo existe durante la vida del nodo.

## Ejemplos



Muestra cómo recorrer la colección de nodos hijos de un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Agregue dos ejecuciones y una forma como nodos hijos al primer párrafo de este documento.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Tenga en cuenta que el 'CustomNodeId' no se guarda en un archivo de salida y solo existe durante la vida del nodo.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itere a través de la colección de hijos inmediatos del párrafo,
// y muestre cualquier ejecución o forma que encontremos dentro.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Ver también

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
