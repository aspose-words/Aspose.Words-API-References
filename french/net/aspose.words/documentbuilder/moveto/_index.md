---
title: DocumentBuilder.MoveTo
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Déplace le curseur vers un nœud en ligne ou à la fin dun paragraphe.
type: docs
weight: 490
url: /fr/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Déplace le curseur vers un nœud en ligne ou à la fin d'un paragraphe.

```csharp
public void MoveTo(Node node)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| node | Node | Le nœud doit être un paragraphe ou un enfant direct d'un paragraphe. |

### Remarques

Quandnœud est un nœud de niveau en ligne, le curseur est déplacé vers ce nœud et du contenu supplémentaire sera inséré avant ce nœud.

Quandnœud est un[`Paragraph`](../../paragraph/), le curseur est déplacé à la fin du paragraphe et du contenu supplémentaire sera inséré juste avant le saut de paragraphe.

Quandnœud est un nœud de niveau bloc mais pas un[`Paragraph`](../../paragraph/), le curseur est déplacé à la fin du premier paragraphe dans node au niveau du bloc et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

### Exemples

Montre comment déplacer la position du curseur d'un DocumentBuilder vers un nœud spécifié.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Le générateur de document a un curseur, qui fait partie du document
// où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de documents.
// Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
// et il se termine également toujours immédiatement après tout nœud que le constructeur vient d'insérer.
// Pour ajouter du contenu à une autre partie du document,
// nous pouvons déplacer le curseur vers un autre nœud avec la méthode "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Le curseur se trouve maintenant devant le nœud vers lequel nous l'avons déplacé.
// L'ajout d'une deuxième exécution l'insérera devant la première exécution.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Déplacez le curseur vers la fin du document pour continuer à ajouter du texte jusqu'à la fin comme auparavant.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


