---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Apprenez à utiliser la méthode EnsureMinimum pour créer automatiquement une section et un paragraphe dans les documents, garantissant ainsi un contenu complet et organisé.
type: docs
weight: 620
url: /fr/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Si le document ne contient aucune section, crée une section avec un paragraphe.

```csharp
public void EnsureMinimum()
```

## Exemples

Montre comment garantir qu'un document contient l'ensemble minimal de nœuds requis pour modifier son contenu.

```csharp
// Un document nouvellement créé contient une section enfant, qui comprend un corps enfant et un paragraphe enfant.
// Nous pouvons modifier le contenu du corps du document en ajoutant des nœuds tels que des exécutions ou des formes en ligne à ce paragraphe.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Il s'agit de l'ensemble minimal de nœuds dont nous avons besoin pour pouvoir modifier le document.
// Nous ne pourrons plus modifier le document si nous supprimons l'un d'entre eux.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Appelez cette méthode pour vous assurer que le document contient au moins ces trois nœuds afin que nous puissions le modifier à nouveau.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
