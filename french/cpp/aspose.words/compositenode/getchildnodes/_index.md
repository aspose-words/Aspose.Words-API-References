---
title: "Méthode Aspose::Words::CompositeNode::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::CompositeNode::GetChildNodes. Retourne une collection dynamique d'éléments enfants qui correspondent au type spécifié en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Spécifie le type de nœuds à sélectionner. |
| isDeep | bool | **true** pour sélectionner parmi tous les nœuds enfants de façon récursive ; **false** pour ne sélectionner que parmi les enfants immédiats. |

### ReturnValue

Une collection dynamique d'enfants du type spécifié.
## Remarques


La collection de nœuds renvoyée par cette méthode est toujours dynamique.

Une collection dynamique est toujours synchronisée avec le document. Par exemple, si vous sélectionnez toutes les sections d'un document et parcourez la collection en supprimant les sections, la section est retirée de la collection immédiatement lorsqu'elle est supprimée du document.

## Exemples



Montre comment imprimer tous les commentaires d'un document et leurs réponses.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Si un commentaire n'a aucun ancêtre, c'est un commentaire de niveau supérieur (« top-level ») contrairement à un commentaire de type réponse.
// Imprime tous les commentaires de niveau supérieur ainsi que les réponses éventuelles.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```


Montre comment extraire des images d'un document et les enregistrer sur le système de fichiers local en tant que fichiers individuels.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Obtenez la collection de formes du document,
// et enregistrez les données d'image de chaque forme contenant une image sous forme de fichier sur le système de fichiers local.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Les données d'image des formes peuvent contenir des images dans de nombreux formats d'image possibles.
        // Nous pouvons déterminer automatiquement une extension de fichier pour chaque image, en fonction de son format.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un [CompositeNode](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vide, par défaut, contient un paragraphe.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Créez trois nœuds de séquence supplémentaires.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Le corps du document n'affichera pas ces séquences tant que nous ne les insérons pas dans un nœud composite
// qui fait lui-même partie de l'arbre de nœuds du document, comme nous l'avons fait avec la première séquence.
// Nous pouvons déterminer où le contenu texte des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion relatif à un autre nœud du paragraphe.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Insérez la deuxième séquence dans le paragraphe devant la séquence initiale.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Insérez la troisième séquence après la séquence initiale.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Insérez la première séquence au début de la collection des nœuds enfants du paragraphe.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Nous pouvons modifier le contenu de la séquence en modifiant et en supprimant les nœuds enfants existants.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Voir aussi

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
