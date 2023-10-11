---
title: DocumentBuilder.MoveToBookmark
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Déplace le curseur vers un signet.
type: docs
weight: 500
url: /fr/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

Déplace le curseur vers un signet.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmarkName | String | Le nom du signet vers lequel déplacer le curseur. |

### Return_Value

`vrai` si le signet a été trouvé ;`FAUX` sinon.

### Remarques

Déplace le curseur vers une position juste après le début du signet portant le nom spécifié the .

La comparaison n'est pas sensible à la casse. Si le signet n'a pas été trouvé,`FAUX` is est renvoyé et le curseur n'est pas déplacé.

L'insertion d'un nouveau texte ne remplace pas le texte existant du signet.

Notez que certains signets dans le document sont affectés à des champs de formulaire. Passer à un tel signet et y insérer du texte insère le texte dans le code du champ de formulaire . Bien que cela n'invalide pas le champ du formulaire, le texte inséré ne sera pas visible car il fait partie du code du champ.

### Exemples

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

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

Déplace le curseur vers un signet avec une plus grande précision.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmarkName | String | Le nom du signet vers lequel déplacer le curseur. |
| isStart | Boolean | Quand`vrai` , déplace le curseur au début du signet. Lorsque`FAUX`, déplace le curseur à la fin du signet. |
| isAfter | Boolean | Quand`vrai` , déplace le curseur après la position de début ou de fin bookmark . Quand`FAUX`, déplace le curseur avant la position de début ou de fin bookmark . |

### Return_Value

`vrai` si le signet a été trouvé ;`FAUX` sinon.

### Remarques

Déplace le curseur vers une position avant ou après le début ou la fin du signet.

Si la position souhaitée n'est pas au niveau en ligne, passe au paragraphe suivant.

La comparaison n'est pas sensible à la casse. Si le signet n'a pas été trouvé,`FAUX` is est renvoyé et le curseur n'est pas déplacé.

### Exemples

Montre comment déplacer le curseur du point d'insertion du nœud d'un générateur de documents vers un signet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un signet valide se compose d'un nœud BookmarkStart, d'un nœud BookmarkEnd avec un
// correspondant au nom du signet quelque part par la suite et au contenu entouré par ces nœuds.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Il existe 4 façons de déplacer le curseur d'un générateur de document vers un signet.
// Si nous sommes entre les nœuds BookmarkStart et BookmarkEnd, le curseur sera à l'intérieur du signet.
// Cela signifie que tout texte ajouté par le constructeur fera partie du signet.
// 1 - En dehors du signet, devant le nœud BookmarkStart :
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - À l'intérieur du signet, juste après le nœud BookmarkStart :
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - À l'intérieur du signet, juste devant le nœud BookmarkEnd :
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - En dehors du signet, après le nœud BookmarkEnd :
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


