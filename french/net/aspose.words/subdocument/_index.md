---
title: Class SubDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.SubDocument classe. Représente un Sousdocument  qui est une référence à un document stocké en externe.
type: docs
weight: 5870
url: /fr/net/aspose.words/subdocument/
---
## SubDocument class

Représente un **Sous-document** - qui est une référence à un document stocké en externe.

```csharp
public class SubDocument : Node
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | Retours **NodeType.SubDocumentNodeType.SubDocument** |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(DocumentVisitor) | Accepte un visiteur. |
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

Dans cette version d'Aspose.Words,`SubDocument` Les nœuds ne fournissent pas de méthodes publiques et de propriétés pour créer ou modifier un sous-document. Dans cette version, vous ne pouvez pas instancier des nœuds SubDocument ou modifier des nœuds existants, sauf en les supprimant.

`SubDocument` ne peut être qu'un enfant de[`Paragraph`](../paragraph/).

### Exemples

Montre comment accéder au sous-document d'un document maître.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Ce nœud sert de référence à un document externe et son contenu n'est pas accessible.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


