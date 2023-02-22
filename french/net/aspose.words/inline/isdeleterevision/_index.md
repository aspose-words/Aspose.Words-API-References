---
title: Inline.IsDeleteRevision
second_title: Référence de l'API Aspose.Words pour .NET
description: Inline propriété. Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.
type: docs
weight: 20
url: /fr/net/aspose.words/inline/isdeleterevision/
---
## Inline.IsDeleteRevision property

Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsDeleteRevision { get; }
```

### Exemples

Montre comment déterminer le type de révision d'un nœud en ligne.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Lorsque nous modifions le document alors que l'option "Suivre les modifications", trouvée dans via Révision -> Suivi,
// est activé dans Microsoft Word, les modifications que nous appliquons comptent comme des révisions.
// Lors de l'édition d'un document à l'aide de Aspose.Words, nous pouvons commencer à suivre les révisions en
// appelant la méthode "StartTrackRevisions" du document et arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
// On peut soit accepter des révisions pour les assimiler dans le document
// ou rejetez-les pour modifier efficacement la modification proposée.
Assert.AreEqual(6, doc.Revisions.Count);

// Le nœud parent d'une révision est l'exécution concernée par la révision. Une exécution est un nœud en ligne.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Vous trouverez ci-dessous cinq types de révisions pouvant marquer un nœud Inline.
// 1 - Une révision "insert":
// Cette révision se produit lorsque nous insérons du texte lors du suivi des modifications.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Une révision "format" :
// Cette révision se produit lorsque nous modifions la mise en forme du texte lors du suivi des modifications.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Une révision "déplacer de":
// Lorsque nous mettons en surbrillance du texte dans Microsoft Word, puis le faisons glisser vers un autre endroit du document
// lors du suivi des modifications, deux révisions apparaissent.
// La révision "move from" est une copie du texte d'origine avant que nous ne le déplacions.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Une révision "déplacer vers" :
// La révision "move to" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "déplacer de" et son texte,
// et conserve le texte de la révision "déplacer vers".
// Le rejet d'une révision de déplacement conserve à l'inverse la révision "déplacer de" et supprime la révision "déplacer vers".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Une révision "supprimer":
// Cette révision se produit lorsque nous supprimons du texte lors du suivi des modifications. Lorsque nous supprimons un texte comme celui-ci,
// il restera dans le document en tant que révision jusqu'à ce que nous acceptions la révision,
// qui supprimera définitivement le texte ou rejettera la révision, ce qui conservera le texte que nous avons supprimé là où il se trouvait.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Voir également

* class [Inline](../)
* espace de noms [Aspose.Words](../../inline/)
* Assemblée [Aspose.Words](../../../)


