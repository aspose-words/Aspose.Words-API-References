---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.RunCollection pour un accès fluide aux nœuds Run. Améliorez le traitement de vos documents grâce à de puissantes fonctionnalités typées !
type: docs
weight: 5570
url: /fr/net/aspose.words/runcollection/
---
## RunCollection class

Fournit un accès typé à une collection de[`Run`](../run/) nœuds.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class RunCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Récupère un[`Run`](../run/) à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une itération simple de style « foreach » sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Copie toutes les exécutions de la collection vers un nouveau tableau d'exécutions. (2 methods) |

## Exemples

Montre comment déterminer le type de révision d'un nœud en ligne.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Lorsque nous éditons le document alors que l'option « Suivi des modifications », trouvée dans via Révision -> Suivi,
// est activé dans Microsoft Word, les modifications que nous appliquons comptent comme des révisions.
// Lors de l'édition d'un document à l'aide d'Aspose.Words, nous pouvons commencer à suivre les révisions en
// invoquer la méthode « StartTrackRevisions » du document et arrêter le suivi en utilisant la méthode « StopTrackRevisions ».
// Nous pouvons soit accepter des révisions pour les assimiler au document
// ou les rejeter pour modifier efficacement le changement proposé.
Assert.AreEqual(6, doc.Revisions.Count);

// Le nœud parent d'une révision est l'exécution concernée par la révision. Une exécution est un nœud en ligne.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Vous trouverez ci-dessous cinq types de révisions qui peuvent signaler un nœud en ligne.
// 1 - Une révision « insert » :
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Une révision de « format » :
// Cette révision se produit lorsque nous modifions la mise en forme du texte tout en suivant les modifications.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Une révision « déplacer de » :
// Lorsque nous mettons en surbrillance du texte dans Microsoft Word, puis que nous le faisons glisser vers un autre emplacement du document
// lors du suivi des modifications, deux révisions apparaissent.
// La révision « déplacer de » est une copie du texte d'origine avant que nous le déplacions.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Une révision « passer à » :
// La révision « déplacer vers » est le texte que nous avons déplacé vers sa nouvelle position dans le document.
// Les révisions « Déplacer de » et « Déplacer vers » apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// L'acceptation d'une révision de déplacement supprime la révision « déplacer de » et son texte,
// et conserve le texte de la révision « déplacer vers ».
// Le rejet d'une révision de déplacement conserve à l'inverse la révision « déplacer de » et supprime la révision « déplacer vers ».
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Une révision « supprimer » :
// Cette révision se produit lorsque nous supprimons du texte lors du suivi des modifications. Lorsque nous supprimons du texte comme ceci,
// il restera dans le document en tant que révision jusqu'à ce que nous acceptions la révision,
// qui supprimera définitivement le texte, ou rejettera la révision, ce qui conservera le texte que nous avons supprimé là où il était.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
