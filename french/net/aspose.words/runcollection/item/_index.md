---
title: RunCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des éléments RunCollection spécifiques. Récupérez n'importe quel index Run by pour une gestion simplifiée des données et des performances améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words/runcollection/item/
---
## RunCollection indexer

Récupère un[`Run`](../../run/) à l'index donné.

```csharp
public Run this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index de la collection. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

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

* class [Run](../../run/)
* class [RunCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
