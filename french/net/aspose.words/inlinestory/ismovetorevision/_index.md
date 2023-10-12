---
title: InlineStory.IsMoveToRevision
second_title: Référence de l'API Aspose.Words pour .NET
description: InlineStory propriété. Retoursvrai si cet objet a été déplacé inséré dans Microsoft Word alors que le suivi des modifications était activé.
type: docs
weight: 60
url: /fr/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveToRevision { get; }
```

### Exemples

Montre comment afficher les propriétés liées aux révisions des nœuds InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Lorsque nous modifions le document pendant que l'option "Suivi des modifications", trouvée dans via Révision -> Suivi,
// est activé dans Microsoft Word, les modifications que nous appliquons comptent comme des révisions.
// Lors de la modification d'un document à l'aide d'Aspose.Words, nous pouvons commencer à suivre les révisions en
// invoque la méthode "StartTrackRevisions" du document et arrête le suivi en utilisant la méthode "StopTrackRevisions".
// On peut soit accepter les révisions pour les assimiler dans le document
// ou rejetez-les pour annuler et ignorer la modification proposée.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Vous trouverez ci-dessous cinq types de révisions pouvant signaler un nœud InlineStory.
// 1 - Une révision "insert":
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Une révision "passer de" :
// Lorsque nous mettons en surbrillance du texte dans Microsoft Word, puis le faisons glisser vers un autre endroit du document
// lors du suivi des modifications, deux révisions apparaissent.
// La révision "déplacer depuis" est une copie du texte d'origine avant son déplacement.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Une révision "déplacer vers" :
// La révision "déplacer vers" est le texte que nous avons déplacé dans sa nouvelle position dans le document.
// Les révisions "Déplacer de" et "Déplacer vers" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// Accepter une révision de déplacement supprime la révision "déplacer depuis" et son texte,
// et conserve le texte de la révision "déplacer vers".
// Le rejet d'une révision de déplacement conserve à l'inverse la révision "déplacer depuis" et supprime la révision "déplacer vers".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Une révision "supprimer" :
// Cette révision se produit lorsque nous supprimons du texte lors du suivi des modifications. Quand nous supprimons un texte comme celui-ci,
// il restera dans le document en tant que révision jusqu'à ce que nous acceptions la révision,
// qui supprimera définitivement le texte, ou rejettera la révision, ce qui conservera le texte que nous avons supprimé là où il se trouvait.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Voir également

* class [InlineStory](../)
* espace de noms [Aspose.Words](../../inlinestory/)
* Assemblée [Aspose.Words](../../../)


