---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Découvrez la méthode NodeCollection Add pour ajouter sans effort des nœuds à votre collection, améliorant ainsi votre gestion des données avec facilité et efficacité.
type: docs
weight: 30
url: /fr/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Ajoute un nœud à la fin de la collection.

```csharp
public void Add(Node node)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| node | Node | Le nœud à ajouter à la fin de la collection. |

### Exceptions

| exception | condition |
| --- | --- |
| NotSupportedException | Le[`NodeCollection`](../) est une collection « profonde ». |

## Remarques

Le nœud est inséré en tant qu’enfant dans l’objet nœud à partir duquel la collection a été créée.

Si le nœud inséré a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document actuel. Le nœud importé peut ensuite être inséré dans le document actuel.

## Exemples

Montre comment préparer un nouveau nœud de section pour l'édition.

```csharp
Document doc = new Document();

// Un document vierge est livré avec une section, qui a un corps, qui à son tour a un paragraphe.
// Nous pouvons ajouter du contenu à ce document en ajoutant des éléments tels que des passages de texte, des formes ou des tableaux à ce paragraphe.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si nous ajoutons une nouvelle section comme celle-ci, elle n'aura pas de corps, ni aucun autre nœud enfant.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Exécutez la méthode « EnsureMinimum » pour ajouter un corps et un paragraphe à cette section pour commencer à la modifier.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [Node](../../node/)
* class [NodeCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
