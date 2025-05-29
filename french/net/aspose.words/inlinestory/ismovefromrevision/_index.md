---
title: InlineStory.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsMoveFromRevision d'InlineStory. Suivez facilement le contenu déplacé ou supprimé dans Microsoft Word grâce au suivi des modifications activé pour une édition fluide.
type: docs
weight: 50
url: /fr/net/aspose.words/inlinestory/ismovefromrevision/
---
## InlineStory.IsMoveFromRevision property

Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveFromRevision { get; }
```

## Exemples

Montre comment afficher les propriétés liées à la révision des nœuds InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Lorsque nous éditons le document alors que l'option « Suivi des modifications », trouvée dans via Révision -> Suivi,
// est activé dans Microsoft Word, les modifications que nous appliquons comptent comme des révisions.
// Lors de l'édition d'un document à l'aide d'Aspose.Words, nous pouvons commencer à suivre les révisions en
// invoquer la méthode « StartTrackRevisions » du document et arrêter le suivi en utilisant la méthode « StopTrackRevisions ».
// Nous pouvons soit accepter des révisions pour les assimiler au document
// ou les rejeter pour annuler et rejeter la modification proposée.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Vous trouverez ci-dessous cinq types de révisions qui peuvent signaler un nœud InlineStory.
// 1 - Une révision « insert » :
// Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Une révision « déplacer de » :
// Lorsque nous mettons en surbrillance du texte dans Microsoft Word, puis que nous le faisons glisser vers un autre emplacement du document
// lors du suivi des modifications, deux révisions apparaissent.
// La révision « déplacer de » est une copie du texte d'origine avant que nous le déplacions.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Une révision « passer à » :
// La révision « déplacer vers » est le texte que nous avons déplacé vers sa nouvelle position dans le document.
// Les révisions « Déplacer de » et « Déplacer vers » apparaissent par paires pour chaque révision de déplacement que nous effectuons.
// L'acceptation d'une révision de déplacement supprime la révision « déplacer de » et son texte,
// et conserve le texte de la révision « déplacer vers ».
// Le rejet d'une révision de déplacement conserve à l'inverse la révision « déplacer de » et supprime la révision « déplacer vers ».
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Une révision « supprimer » :
// Cette révision se produit lorsque nous supprimons du texte lors du suivi des modifications. Lorsque nous supprimons du texte comme ceci,
// il restera dans le document en tant que révision jusqu'à ce que nous acceptions la révision,
// qui supprimera définitivement le texte, ou rejettera la révision, ce qui conservera le texte que nous avons supprimé là où il était.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Voir également

* class [InlineStory](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
