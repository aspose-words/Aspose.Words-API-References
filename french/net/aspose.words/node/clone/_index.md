---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words pour .NET
description: Node Clone méthode. Crée un duplicata du nœud en C#.
type: docs
weight: 100
url: /fr/net/aspose.words/node/clone/
---
## Node.Clone method

Crée un duplicata du nœud.

```csharp
public Node Clone(bool isCloneChildren)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| isCloneChildren | Boolean | True pour cloner de manière récursive le sous-arbre sous le nœud spécifié ; false pour cloner uniquement le nœud lui-même. |

### Return_Value

Le nœud cloné.

## Remarques

Cette méthode sert de constructeur de copie pour les nœuds. Le nœud cloné n'a pas de parent, mais appartient au même document que le nœud d'origine.

Cette méthode effectue toujours une copie complète du nœud. Le*isCloneChildren* paramètre spécifie s'il faut également copier tous les nœuds enfants.

## Exemples

Montre comment cloner un nœud composite.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Vous trouverez ci-dessous deux façons de cloner un nœud composite.
// 1 - Créez un clone d'un nœud et créez également un clone de chacun de ses nœuds enfants.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Créez un clone d'un nœud seul, sans aucun enfant.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Voir également

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
