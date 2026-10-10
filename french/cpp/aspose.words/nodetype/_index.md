---
title: "Aspose::Words::NodeType enum"
linktitle: "NodeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::NodeType. Spécifie le type d'un nœud de document Word en C++."
type: docs
weight: 102000
url: /fr/cpp/aspose.words/nodetype/
---
## NodeType enum


Spécifie le type d'un nœud de document Word.

```cpp
enum class NodeType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Any | 0 | Indique tous les types de nœuds. Permet de sélectionner tous les enfants. |
| Document | 1 | Un objet [Document](../document/) qui, en tant que racine de l'arbre du document, donne accès à l'ensemble du document Word. Un nœud [Document](../document/) peut contenir des nœuds [Section](../section/). |
| Section | 2 | Un objet [Section](../section/) qui correspond à une section d'un document Word. Un nœud [Section](../section/) peut contenir des nœuds [Body](../body/) et [HeaderFooter](../headerfooter/). |
| Body | 3 | Un objet [Body](../body/) qui contient le texte principal d'une section (histoire de texte principal). Un nœud [Body](../body/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| HeaderFooter | 4 | Un objet [HeaderFooter](../headerfooter/) qui contient le texte d'un en-tête ou pied de page particulier dans une section. Un nœud [HeaderFooter](../headerfooter/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| Table | 5 | Un objet [Table](../../aspose.words.tables/table/) qui représente un tableau dans un document Word. Un nœud [Table](../../aspose.words.tables/table/) peut contenir des nœuds [Row](../../aspose.words.tables/row/). |
| Row | 6 | Une ligne d'un tableau. Un nœud [Row](../../aspose.words.tables/row/) peut contenir des nœuds [Cell](../../aspose.words.tables/cell/). |
| Cell | 7 | Une cellule d'une ligne de tableau. Un nœud [Cell](../../aspose.words.tables/cell/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| Paragraph | 8 | Un paragraphe de texte. Un nœud [Paragraph](../paragraph/) est un conteneur pour les éléments en ligne [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), ainsi que [BookmarkStart](../bookmarkstart/) et [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | Un début d'un marqueur de signet. |
| BookmarkEnd | 10 | Une fin d'un marqueur de signet. |
| EditableRangeStart | 11 | Un début d'une plage modifiable. |
| EditableRangeEnd | 12 | Une fin d'une plage modifiable. |
| MoveFromRangeStart | 13 | Un début d'une plage MoveFrom. |
| MoveFromRangeEnd | 14 | Une fin d'une plage MoveFrom. |
| MoveToRangeStart | 15 | Un début d'une plage MoveTo. |
| MoveToRangeEnd | 16 | Une fin d'une plage MoveTo. |
| GroupShape | 17 | Un groupe de formes, d'images, d'objets OLE ou d'autres formes de groupe. Un nœud [GroupShape](../../aspose.words.drawing/groupshape/) peut contenir d'autres nœuds [Shape](../../aspose.words.drawing/shape/) et [GroupShape](../../aspose.words.drawing/groupshape/). |
| Shape | 18 | Un objet de dessin, tel qu'une forme OfficeArt, une image ou un objet OLE. Un nœud [Shape](../../aspose.words.drawing/shape/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| Comment | 19 | Un commentaire dans un document Word. Un nœud [Comment](../comment/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| Footnote | 20 | Une note de bas de page ou de fin dans un document Word. Un nœud [Footnote](../../aspose.words.notes/footnote/) peut contenir des nœuds [Paragraph](../paragraph/) et [Table](../../aspose.words.tables/table/). |
| Run | 21 | Une séquence de texte. |
| FieldStart | 22 | Un caractère spécial qui désigne le début d'un champ Word. |
| FieldSeparator | 23 | Un caractère spécial qui sépare le code du champ du résultat du champ. |
| FieldEnd | 24 | Un caractère spécial qui désigne la fin d'un champ Word. |
| FormField | 25 | Un champ de formulaire. |
| SpecialChar | 26 | Un caractère spécial qui n'est pas l'un des types de caractères spéciaux plus spécifiques. |
| SmartTag | 27 | Une balise intelligente autour d'une ou plusieurs structures en ligne (séquences, images, champs, etc.) dans un paragraphe. |
| StructuredDocumentTag | 28 | Permet de définir des informations spécifiques au client et leurs moyens de présentation. |
| StructuredDocumentTagRangeStart | 29 | Un début d'une balise de document structuré **ranged** qui accepte du contenu multi‑sections. |
| StructuredDocumentTagRangeEnd | 30 | Une fin d'une balise de document structuré **ranged** qui accepte du contenu multi‑sections. |
| GlossaryDocument | 31 | Un document de glossaire dans le document principal. |
| BuildingBlock | 32 | Un bloc de construction dans un document de glossaire (par ex. entrée de document de glossaire). |
| CommentRangeStart | 33 | Un nœud marqueur qui représente le début d’une plage commentée. |
| CommentRangeEnd | 34 | Un nœud marqueur qui représente la fin d’une plage commentée. |
| OfficeMath | 35 | Un objet Office [Math](../../aspose.words.math/). Peut être une équation, une fonction, une matrice ou l’un des autres objets mathématiques. Peut être une collection d’objets mathématiques et peut également contenir des objets non mathématiques tels que des séquences de texte. |
| SubDocument | 36 | Un nœud sous-document qui est un lien vers un autre document. |
| System | 37 | Réservé à un usage interne par [Aspose.Words](../). |
| Null | 38 | Réservé à un usage interne par [Aspose.Words](../). |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
