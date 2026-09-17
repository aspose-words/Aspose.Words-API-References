---
title: "Aspose::Words::Node::get_CustomNodeId méthode"
linktitle: "get_CustomNodeId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::get_CustomNodeId méthode. Spécifie un identifiant de nœud personnalisé en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/node/get_customnodeid/
---
## Node::get_CustomNodeId method


Spécifie un identifiant de nœud personnalisé.

```cpp
int32_t Aspose::Words::Node::get_CustomNodeId() const
```

## Remarques


La valeur par défaut est zéro.

Cet identifiant peut être défini et utilisé arbitrairement. Par exemple, comme clé pour obtenir des données externes.

Note importante, la valeur spécifiée n'est pas enregistrée dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.

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

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
