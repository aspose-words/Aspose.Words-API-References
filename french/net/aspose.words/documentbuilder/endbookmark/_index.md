---
title: DocumentBuilder.EndBookmark
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Marque la position actuelle dans le document comme fin de signet.
type: docs
weight: 190
url: /fr/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Marque la position actuelle dans le document comme fin de signet.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmarkName | String | Nom du signet. |

### Return_Value

Le nœud de fin de signet qui vient d'être créé.

### Remarques

Les signets d'un document peuvent se chevaucher et s'étendre sur n'importe quelle plage. Pour créer un signet valide, vous devez appeler les deux[`StartBookmark`](../startbookmark/) et`EndBookmark` avec le même **bookmarkName** paramètre .

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

### Exemples

Montre comment créer un signet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un signet valide doit avoir le texte du corps du document entouré par
// Nœuds BookmarkStart et BookmarkEnd créés avec un nom de signet correspondant.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Montre comment insérer un lien hypertexte qui fait référence à un signet local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Insère un champ HYPERLINK qui renvoie au signet. Nous pouvons passer des commutateurs de champ
// à la méthode "InsertHyperlink" dans le cadre de l'argument contenant le nom du signet référencé.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Voir également

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


