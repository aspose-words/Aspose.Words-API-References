---
title: Class RunCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.RunCollection classe. Fournit un accès typé à une collection deRun nœuds.
type: docs
weight: 4830
url: /fr/net/aspose.words/runcollection/
---
## RunCollection class

Fournit un accès typé à une collection de[`Run`](../run/) nœuds.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article documentaire.

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
| [Add](../../aspose.words/nodecollection/add/)(Node) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Détermine si un nœud fait partie de la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Copie toutes les exécutions de la collection vers un nouveau tableau d'exécutions. (2 methods) |

### Exemples

Montre comment déterminer le type de révision d’un nœud en ligne.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Lorsque nous modifions le document pendant que l'option "Suivi des modifications", trouvée dans via Révision -> Suivi,
// est activé dans Microsoft Word, les modifications que nous appliquons comptent comme des révisions.
// Lors de la modification d'un document à l'aide d'Aspose.Words, nous pouvons commencer à suivre les révisions en
// invoque la méthode "StartTrackRevisions" du document et arrête le suivi en utilisant la méthode "StopTrackRevisions".
// On peut soit accepter les révisions pour les assimiler dans le document
// ou rejetez-les pour modifier efficacement le changement proposé.
Assert.AreEqual(6, doc.Revisions.Count);

// Le nœud parent d'une révision est l'exécution concernée par la révision. Une exécution est un nœud en ligne.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Vous trouverez ci-dessous cinq types de révisions pouvant signaler un nœud Inline.
// 1 - Une révision "insert":
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Une révision "format" :
// Cette révision se produit lorsque nous modifions le formatage du texte tout en suivant les modifications.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Une révision "passer de" :
// Lorsque nous mettons en surbrillance du texte dans Microsoft Word, puis le faisons glisser vers un autre endroit du document
// lors du suivi des modifications, deux révisions apparaissent.
// La révision "déplacer depuis" est une copie du texte d'origine avant son déplacement.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Une révision "passer à" :
// La révision "déplacer vers" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Déplacer de" et "Déplacer vers" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "déplacer depuis" et son texte,
// et conserve le texte de la révision "déplacer vers".
// Le rejet d'une révision de déplacement conserve à l'inverse la révision "déplacer depuis" et supprime la révision "déplacer vers".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Une révision "supprimer":
// Cette révision se produit lorsque nous supprimons du texte lors du suivi des modifications. Quand nous supprimons un texte comme celui-ci,
// il restera dans le document en tant que révision jusqu'à ce que nous acceptions la révision,
// qui supprimera définitivement le texte, ou rejettera la révision, ce qui conservera le texte que nous avons supprimé là où il se trouvait.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


