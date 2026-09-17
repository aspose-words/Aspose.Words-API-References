---
title: "Aspose::Words::CompositeNode::GetChild méthode"
linktitle: "GetChild"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::GetChild méthode. Retourne le nième nœud enfant qui correspond au type spécifié en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


Renvoie le nième nœud enfant qui correspond au type spécifié.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Spécifie le type du nœud enfant. |
| index | int32_t | Indice basé sur zéro du nœud enfant à sélectionner. Les indices négatifs sont également autorisés et indiquent un accès depuis la fin, c’est‑à‑dire -1 signifie le dernier nœud. |
| isDeep | bool | **true** pour sélectionner parmi tous les nœuds enfants de façon récursive ; **false** pour sélectionner uniquement parmi les enfants immédiats. Voir les remarques pour plus d’informations. |

### ReturnValue

Le nœud enfant qui correspond aux critères ou **null** si aucun nœud correspondant n’est trouvé.
## Remarques


Si l’indice est hors limites, un **null** est renvoyé.

## Exemples



Montre comment parcourir la collection de nœuds enfants d'un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ajoutez deux exécutions et une forme en tant que nœuds enfants au premier paragraphe de ce document.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Notez que le 'CustomNodeId' n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itérez à travers la collection d'enfants immédiats du paragraphe,
// et affichez tous les runs ou formes que nous y trouvons.
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

## Voir aussi

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
