---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode CompositeNode PrependChild améliore votre structure de données en ajoutant efficacement des nœuds au début de votre liste de nœuds enfants.
type: docs
weight: 170
url: /fr/net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild&lt;T&gt; method

Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud.

```csharp
public T PrependChild<T>(T newChild)
    where T : Node
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| newChild | T | Le nœud à ajouter. |

### Return_Value

Le nœud a été ajouté.

## Remarques

Si le*newChild* est déjà dans l'arbre, il est d'abord supprimé.

Si le nœud inséré a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document actuel. Le nœud importé peut ensuite être inséré dans le document actuel.

## Exemples

Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un CompositeNode.

```csharp
Document doc = new Document();

// Un document vide, par défaut, comporte un paragraphe.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Créez trois nœuds d'exécution supplémentaires.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Le corps du document n'affichera pas ces exécutions tant que nous ne les aurons pas insérées dans un nœud composite
// qui fait lui-même partie de l'arborescence des nœuds du document, comme nous l'avons fait lors de la première exécution.
// Nous pouvons déterminer où se trouve le contenu textuel des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion par rapport à un autre nœud du paragraphe.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insérer la deuxième exécution dans le paragraphe devant l'exécution initiale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insérer la troisième exécution après l'exécution initiale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insérer la première exécution au début de la collection de nœuds enfants du paragraphe.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Nous pouvons modifier le contenu de l'exécution en modifiant et en supprimant les nœuds enfants existants.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
