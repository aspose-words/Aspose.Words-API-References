---
title: "Metodo Aspose::Words::CompositeNode::GetChild"
linktitle: "GetChild"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::GetChild. Restituisce il nodo figlio N‑esimo che corrisponde al tipo specificato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Specifica il tipo del nodo figlio. |
| index | int32_t | Indice basato su zero del nodo figlio da selezionare. Sono consentiti anche indici negativi che indicano l'accesso dalla fine, ad esempio -1 indica l'ultimo nodo. |
| isDeep | bool | **true** per selezionare tutti i nodi figlio ricorsivamente; **false** per selezionare solo tra i figli immediati. Vedi le note per ulteriori informazioni. |

### ReturnValue

Il nodo figlio che corrisponde ai criteri o **null** se non viene trovato alcun nodo corrispondente.
## Note


Se l'indice è fuori intervallo, viene restituito **null**.

## Esempi



Mostra come attraversare la collezione di nodi figlio di un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aggiungi due run e una shape come nodi figlio al primo paragrafo di questo documento.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo durante la vita del nodo.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itera attraverso la collezione di figli immediati del paragrafo,
// e stampa tutti i run o le shape che troviamo al suo interno.
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

## Vedi anche

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
