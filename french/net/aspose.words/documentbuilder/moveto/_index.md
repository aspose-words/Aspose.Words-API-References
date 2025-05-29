---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words pour .NET
description: Découvrez la méthode MoveTo de DocumentBuilder pour naviguer facilement dans les nœuds en ligne et positionner efficacement votre curseur aux extrémités des paragraphes pour une édition transparente du document.
type: docs
weight: 520
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

## Remarques

Quandnœud est un nœud de niveau en ligne, le curseur est déplacé vers ce nœud et un contenu supplémentaire sera inséré avant ce nœud.

Quandnœud est un[`Paragraph`](../../paragraph/)le curseur est déplacé à la fin du paragraphe et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

Quandnœud est un nœud de niveau bloc mais pas un[`Paragraph`](../../paragraph/), le curseur est déplacé à la fin du premier paragraphe dans le nœud de niveau bloc et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

## Exemples

Montre comment déplacer la position du curseur d'un DocumentBuilder vers un nœud spécifié.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Le générateur de documents dispose d'un curseur, qui agit comme une partie du document
// où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de documents.
// Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
// et il se termine également toujours immédiatement après tout nœud que le constructeur vient d'insérer.
// Pour ajouter du contenu à une autre partie du document,
// nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
// L'ajout d'une deuxième exécution l'insérera devant la première exécution.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
