---
title: DocumentBuilder.IsAtEndOfParagraph
linktitle: IsAtEndOfParagraph
articleTitle: IsAtEndOfParagraph
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsAtEndOfParagraph de DocumentBuilder, qui vérifie efficacement si le curseur est positionné à la fin d'un paragraphe pour une édition transparente du document.
type: docs
weight: 110
url: /fr/net/aspose.words/documentbuilder/isatendofparagraph/
---
## DocumentBuilder.IsAtEndOfParagraph property

Retours`vrai` si le curseur est à la fin du paragraphe actuel.

```csharp
public bool IsAtEndOfParagraph { get; }
```

## Exemples

Montre comment déplacer le curseur d'un générateur de documents vers différents nœuds d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créer un signet valide, une entité composée de nœuds entourés d'un nœud de départ de signet,
 // et un nœud de fin de signet.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Le curseur du générateur de documents est toujours en avance sur le nœud que nous avons ajouté en dernier avec lui.
// Si le curseur du générateur est à la fin du document, son nœud actuel sera nul.
// Le nœud précédent est le nœud de fin de signet que nous avons ajouté en dernier.
// L'ajout de nouveaux nœuds avec le générateur les ajoutera au dernier nœud.
Assert.Null(builder.CurrentNode);

// Si nous souhaitons éditer une autre partie du document avec le générateur,
// nous devrons amener son curseur sur le nœud que nous souhaitons éditer.
builder.MoveToBookmark("MyBookmark");

// Le déplacer vers un signet le déplacera vers le premier nœud dans les nœuds de début et de fin du signet, l'exécution incluse.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Nous pouvons également déplacer le curseur vers un nœud individuel comme celui-ci.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Nous pouvons utiliser des méthodes spécifiques pour nous déplacer au début/à la fin d'un document.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
