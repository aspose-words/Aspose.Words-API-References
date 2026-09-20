---
title: "Método Aspose::Words::CompositeNode::GetChild"
linktitle: "GetChild"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::CompositeNode::GetChild. Devuelve el enésimo nodo hijo que coincide con el tipo especificado en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Especifica el tipo del nodo hijo. |
| index | int32_t | Índice basado en cero del nodo hijo a seleccionar. También se permiten índices negativos que indican acceso desde el final, es decir, -1 significa el último nodo. |
| isDeep | bool | **true** para seleccionar de todos los nodos hijos de forma recursiva; **false** para seleccionar solo entre los hijos inmediatos. Consulte las observaciones para más información. |

### ReturnValue

El nodo hijo que coincide con el criterio o **null** si no se encuentra ningún nodo coincidente.
## Observaciones


Si el índice está fuera de rango, se devuelve **null**.

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

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
