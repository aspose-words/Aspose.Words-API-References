---
title: Inline
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de base pour les nœuds de niveau en ligne qui peuvent être associés à un formatage de caractères mais ne peuvent pas avoir de nœuds enfants.
type: docs
weight: 3060
url: /fr/net/aspose.words/inline/
---
## Inline class

Classe de base pour les nœuds de niveau en ligne qui peuvent être associés à un formatage de caractères, mais ne peuvent pas avoir de nœuds enfants.

```csharp
public abstract class Inline : Node
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [Font](../../aspose.words/inline/font/) { get; } | Fournit l'accès à la mise en forme de la police de cet objet. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Une classe dérivée de **En ligne** peut être un enfant de **Paragraphe**.

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

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
