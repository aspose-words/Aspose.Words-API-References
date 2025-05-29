---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Inline, conçue pour la mise en forme des caractères dans les nœuds en ligne. Améliorez le style de votre document sans nœuds enfants !
type: docs
weight: 3710
url: /fr/net/aspose.words/inline/
---
## Inline class

Classe de base pour les nœuds de niveau en ligne qui peuvent avoir un formatage de caractères associé, mais ne peuvent pas avoir leurs propres nœuds enfants.

Pour en savoir plus, visitez le[Niveaux logiques des nœuds dans un document](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) article de documentation.

```csharp
public abstract class Inline : Node
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [Font](../../aspose.words/inline/font/) { get; } | Donne accès à la mise en forme de la police de cet objet. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Retours`vrai` si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

Une classe dérivée de`Inline` peut être un enfant de[`Paragraph`](../paragraph/).

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

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
