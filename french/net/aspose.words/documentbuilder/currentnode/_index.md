---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: Aspose.Words pour .NET
description: DocumentBuilder CurrentNode propriété. Obtient le nœud actuellement sélectionné dans ce DocumentBuilder en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Obtient le nœud actuellement sélectionné dans ce DocumentBuilder.

```csharp
public Node CurrentNode { get; }
```

## Remarques

`CurrentNode` est un curseur de[`DocumentBuilder`](../) et pointe vers un[`Node`](../../node/) qui est un enfant direct d'un[`Paragraph`](../../paragraph/) . Toutes les opérations d'insertion que vous effectuez en utilisant [`DocumentBuilder`](../) sera inséré avant le`CurrentNode`.

Lorsque le paragraphe courant est vide ou que le curseur est positionné juste avant la fin d'une balise de paragraphe ou de document structuré,`CurrentNode` Retour`nul`.

## Exemples

Montre comment déplacer le curseur d'un générateur de document vers différents nœuds d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un signet valide, une entité composée de nœuds entourés d'un nœud de début de signet,
 // et un nœud de fin de signet.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Le curseur du générateur de document est toujours devant le nœud que nous avons ajouté en dernier avec lui.
// Si le curseur du constructeur est à la fin du document, son nœud courant sera nul.
// Le nœud précédent est le nœud de fin du signet que nous avons ajouté en dernier.
// L'ajout de nouveaux nœuds avec le constructeur les ajoutera au dernier nœud.
Assert.Null(builder.CurrentNode);

// Si l'on souhaite éditer une autre partie du document avec le builder,
// nous devrons amener son curseur sur le nœud que nous souhaitons éditer.
builder.MoveToBookmark("MyBookmark");

// Le déplacer vers un signet le déplacera vers le premier nœud des nœuds de début et de fin du signet, l'exécution ci-jointe.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Nous pouvons également déplacer le curseur vers un nœud individuel comme celui-ci.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// On peut utiliser des méthodes spécifiques pour se déplacer au début/fin d'un document.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Voir également

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
