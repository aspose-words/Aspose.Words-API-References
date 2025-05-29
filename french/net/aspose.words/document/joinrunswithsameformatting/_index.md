---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode JoinRunsWithSameFormatting fusionne de manière transparente le texte formaté dans les paragraphes de votre document pour un aspect professionnel et soigné.
type: docs
weight: 660
url: /fr/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Les jointures s'exécutent avec le même formatage dans tous les paragraphes du document.

```csharp
public int JoinRunsWithSameFormatting()
```

### Return_Value

Nombre de jointures effectuées. Quand**N** les pistes adjacentes sont jointes, elles comptent comme**N - 1** rejoint.

## Remarques

Il s'agit d'une méthode d'optimisation. Certains documents contiennent des exécutions adjacentes avec le même formatage. Cela se produit généralement si un document a été modifié manuellement de manière intensive. Vous pouvez réduire la taille du document et accélérer le traitement ultérieur en joignant ces exécutions.

L'opération vérifie chaque[`Paragraph`](../../paragraph/) nœud dans le document pour adjacent[`Run`](../../run/)Nœuds ayant des propriétés identiques. Les identifiants uniques utilisés pour suivre les sessions d'édition de création et de modification de run sont ignorés. La première exécution de chaque séquence de jointure accumule tout le texte. Les exécutions restantes sont supprimées du document.

## Exemples

Montre comment joindre des exécutions dans un document pour réduire les exécutions inutiles.

```csharp
// Ouvrir un document contenant des séquences de texte adjacentes avec un formatage identique,
// ce qui se produit généralement si nous modifions le même paragraphe plusieurs fois dans Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Si un certain nombre de ces exécutions sont adjacentes avec un formatage identique,
// alors le document peut être simplifié.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Combinez ces exécutions avec cette méthode et vérifiez le nombre de jointures d'exécution qui auront lieu.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Le nombre de jointures et le nombre d'exécutions que nous avons après la jointure
// devrait additionner le nombre d'exécutions que nous avons eues initialement.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
