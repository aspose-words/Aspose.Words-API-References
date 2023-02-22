---
title: DocumentBuilder.IsAtStartOfParagraph
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder propriété. Renvoie true si le curseur est au début du paragraphe courant pas de texte avant le curseur.
type: docs
weight: 110
url: /fr/net/aspose.words/documentbuilder/isatstartofparagraph/
---
## DocumentBuilder.IsAtStartOfParagraph property

Renvoie true si le curseur est au début du paragraphe courant (pas de texte avant le curseur).

```csharp
public bool IsAtStartOfParagraph { get; }
```

### Exemples

Montre comment déplacer le curseur d'un générateur de document vers différents nœuds dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un signet valide, une entité composée de nœuds entourés d'un nœud de début de signet,
 // et un nœud de fin de signet.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Le curseur du générateur de document est toujours devant le nœud que nous avons ajouté en dernier avec lui.
// Si le curseur du constructeur est à la fin du document, son nœud courant sera nul.
// Le nœud précédent est le dernier nœud de signet que nous avons ajouté en dernier.
// L'ajout de nouveaux nœuds avec le constructeur les ajoutera au dernier nœud.
Assert.Null(builder.CurrentNode);

// Si l'on souhaite éditer une autre partie du document avec le constructeur,
// nous devrons amener son curseur sur le nœud que nous souhaitons éditer.
builder.MoveToBookmark("MyBookmark");

// Le déplacer vers un signet le déplacera vers le premier nœud dans les nœuds de début et de fin du signet, la série jointe.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Nous pouvons également déplacer le curseur vers un nœud individuel comme celui-ci.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Nous pouvons utiliser des méthodes spécifiques pour passer au début/à la fin d'un document.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


