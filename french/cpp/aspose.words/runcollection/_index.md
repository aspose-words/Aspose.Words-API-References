---
title: "Aspose::Words::RunCollection classe"
linktitle: "RunCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RunCollection classe. Fournit un accès typé à une collection de nœuds Run. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 57000
url: /fr/cpp/aspose.words/runcollection/
---
## RunCollection class


Fournit un accès typé à une collection de nœuds [Run](../run/). Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class RunCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Récupère un [Run](../run/) à l'index donné. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie tous les runs de la collection dans un nouveau tableau de runs. |
| static [Type](./type/)() |  |

## Exemples



Montre comment déterminer le type de révision d'un nœud en ligne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
// est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
// Lors de l'édition d'un document avec Aspose.Words, nous pouvons commencer le suivi des révisions en
// appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
// Nous pouvons soit accepter les révisions pour les intégrer au document
// ou les rejeter afin de modifier efficacement le changement proposé.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Le nœud parent d'une révision est le run auquel la révision se rapporte. Un Run est un nœud Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Ci-dessous se trouvent cinq types de révisions qui peuvent marquer un nœud Inline.
// 1 -  Une révision "insert" :
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Une révision "format" :
// Cette révision se produit lorsque nous modifions le formatage du texte tout en suivant les modifications.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Une révision "move from" :
// Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
// tout en suivant les modifications, deux révisions apparaissent.
// La révision "move from" est une copie du texte original avant que nous le déplacions.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Une révision "move to" :
// La révision "move to" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
// et conserve le texte de la révision "move to".
// Rejeter une révision de déplacement, au contraire, conserve la révision "move from" et supprime la révision "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Une révision "delete" :
// Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
// il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions,
// ce qui supprimera définitivement le texte, ou que nous rejetions la révision, ce qui conservera le texte que nous avons supprimé à son emplacement d'origine.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Voir aussi

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
