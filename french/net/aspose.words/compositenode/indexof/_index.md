---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words pour .NET
description: CompositeNode IndexOf méthode. Renvoie lindex du nœud enfant spécifié dans le tableau de nœuds enfants en C#.
type: docs
weight: 120
url: /fr/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants.

```csharp
public int IndexOf(Node child)
```

## Remarques

Renvoie -1 si le nœud n'est pas trouvé dans les nœuds enfants.

## Exemples

Montre comment obtenir l'index d'un nœud enfant donné à partir de son parent.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Récupère l'index du dernier paragraphe du corps de la première section.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
