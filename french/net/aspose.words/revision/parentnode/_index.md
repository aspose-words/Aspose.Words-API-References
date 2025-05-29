---
title: Revision.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Revision ParentNode, qui identifie le nœud parent direct de tout type de révision, à l'exception de StyleDefinitionChange. Améliorez votre efficacité de codage !
type: docs
weight: 40
url: /fr/net/aspose.words/revision/parentnode/
---
## Revision.ParentNode property

Obtient le nœud parent immédiat (propriétaire) de cette révision. Cette propriété fonctionnera pour tout type de révision autre queStyleDefinitionChange .

```csharp
public Node ParentNode { get; }
```

## Remarques

Si cette révision concerne un changement de formatage de style, utilisez[`ParentStyle`](../parentstyle/) à la place.

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

* class [Node](../../node/)
* class [Revision](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
