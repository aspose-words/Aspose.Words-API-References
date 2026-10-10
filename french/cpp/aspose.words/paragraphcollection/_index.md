---
title: "Classe Aspose::Words::ParagraphCollection"
linktitle: "ParagraphCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::ParagraphCollection. Fournit un accès typé à une collection de nœuds Paragraph. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 48000
url: /fr/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Fournit un accès typé à une collection de nœuds [Paragraph](../paragraph/). Pour en savoir plus, consultez l'article de documentation [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](../nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](../nodecollection/get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère un [Paragraph](../paragraph/) à l'index donné. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie tous les paragraphes de la collection dans un nouveau tableau de paragraphes. |
| static [Type](./type/)() |  |

## Exemples



Montre comment vérifier si un paragraphe est une révision de déplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Ce document contient des révisions \"Move\", qui apparaissent lorsque nous sélectionnons du texte avec le curseur,
// et que nous le faisons glisser pour le déplacer vers un autre emplacement
// tout en suivant les révisions dans Microsoft Word via \"Review\" -> \"Track changes\".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Les révisions de déplacement sont constituées de paires de révisions \"Move from\" et \"Move to\".
// Ces révisions sont des modifications potentielles du document que nous pouvons soit accepter, soit rejeter.
// Avant d'accepter/rejeter une révision de déplacement, le document
// doit garder une trace à la fois des destinations de départ et d'arrivée du texte.
// Le deuxième et le quatrième paragraphe définissent une telle révision, et donc les deux ont le même contenu.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// La révision \"Move from\" est le paragraphe d'où nous avons fait glisser le texte.
// Si nous acceptons la révision, ce paragraphe disparaîtra,
// et l'autre restera et ne sera plus une révision.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// La révision \"Move to\" est le paragraphe vers lequel nous avons fait glisser le texte.
// Si nous rejetons la révision, ce paragraphe disparaîtra à la place, et l'autre restera.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Voir aussi

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
