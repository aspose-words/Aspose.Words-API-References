---
title: "Aspose::Words::InlineStory::get_IsDeleteRevision méthode"
linktitle: "get_IsDeleteRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::InlineStory::get_IsDeleteRevision méthode. Retourne true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/inlinestory/get_isdeleterevision/
---
## InlineStory::get_IsDeleteRevision method


Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::InlineStory::get_IsDeleteRevision()
```


## Exemples



Montre comment afficher les propriétés liées aux révisions des nœuds [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
// est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
// Lors de l'édition d'un document avec Aspose.Words, nous pouvons commencer le suivi des révisions en
// appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
// Nous pouvons soit accepter les révisions pour les intégrer au document
// ou les rejeter pour annuler et supprimer le changement proposé.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Ci-dessous, cinq types de révisions pouvant marquer un nœud InlineStory.
// 1 -  Une révision "insert" :
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  Une révision \"move from\" :
// Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
// tout en suivant les modifications, deux révisions apparaissent.
// La révision "move from" est une copie du texte original avant que nous le déplacions.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  Une révision \"move to\" :
// La révision "move to" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
// et conserve le texte de la révision "move to".
// Rejeter une révision de déplacement, au contraire, conserve la révision "move from" et supprime la révision "move to".
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  Une révision \"delete\" :
// Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
// il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions,
// ce qui supprimera définitivement le texte, ou que nous rejetions la révision, ce qui conservera le texte que nous avons supprimé à son emplacement d'origine.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Voir aussi

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
