---
title: BookmarksOutlineLevelCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words pour .NET
description: Découvrez si un signet existe dans BookmarksOutlineLevelCollection. Gérez facilement vos signets grâce à cette méthode essentielle pour une organisation efficace.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/bookmarksoutlinelevelcollection/contains/
---
## BookmarksOutlineLevelCollection.Contains method

Détermine si la collection contient un signet portant le nom donné.

```csharp
public bool Contains(string name)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom du signet à localiser, insensible à la casse. |

### Return_Value

`vrai`si l'élément est trouvé dans la collection ; sinon,`FAUX`.

## Exemples

Montre comment définir les niveaux de contour des signets.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un signet avec un autre signet imbriqué à l'intérieur.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Insérer un autre signet.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// Lors de l'enregistrement au format .pdf, les signets sont accessibles via un menu déroulant et utilisés comme ancres par la plupart des lecteurs.
// Les signets peuvent également avoir des valeurs numériques pour les niveaux de plan,
// activer les entrées de plan de niveau inférieur pour masquer les entrées enfants de niveau supérieur lorsqu'elles sont réduites dans le lecteur.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Nous pouvons supprimer deux éléments afin qu'il ne reste que la désignation du niveau de plan pour « Signet 1 ».
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Il existe neuf niveaux de plan. Leur numérotation sera optimisée lors de la sauvegarde.
// Dans ce cas, les niveaux « 5 » et « 9 » deviendront « 2 » et « 3 ».
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vider cette collection préservera les signets et les placera tous au même niveau de plan.
outlineLevels.Clear();
```

### Voir également

* class [BookmarksOutlineLevelCollection](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
