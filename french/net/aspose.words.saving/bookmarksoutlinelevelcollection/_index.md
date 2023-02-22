---
title: Class BookmarksOutlineLevelCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection classe. Une collection de niveaux hiérarchiques de signets individuels.
type: docs
weight: 4590
url: /fr/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Une collection de niveaux hiérarchiques de signets individuels.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Obtient ou définit un niveau hiérarchique de signet par le nom du signet. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(string, int) | Ajoute un signet à la collection. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Supprime tous les éléments de la collection. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(string) | Détermine si la collection contient un signet avec le nom donné. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() |  |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(string) | Renvoie l'index de base zéro du signet spécifié dans la collection. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(string) | Supprime un signet portant le nom spécifié de la collection. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(int) | Supprime un signet à l'index spécifié. |

### Remarques

Key est un nom de signet de chaîne insensible à la casse. La valeur est un niveau hiérarchique de signet int.

Le niveau de plan du signet peut être une valeur comprise entre 0 et 9. Spécifiez 0 et le signet Word ne s'affichera pas dans le plan du document. Spécifiez 1 et le signet Word s'affichera dans le plan du document au niveau 1 ; 2 pour le niveau 2 et ainsi de suite.

### Exemples

Montre comment définir des niveaux hiérarchiques pour les signets.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un signet avec un autre signet imbriqué à l'intérieur.
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
// Les signets peuvent également avoir des valeurs numériques pour les niveaux hiérarchiques,
// activation des entrées de plan de niveau inférieur pour masquer les entrées enfants de niveau supérieur lorsqu'elles sont réduites dans le lecteur.
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

// Nous pouvons supprimer deux éléments afin qu'il ne reste que la désignation de niveau hiérarchique pour "Signet 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Il existe neuf niveaux hiérarchiques. Leur numérotation sera optimisée lors de l'opération de sauvegarde.
// Dans ce cas, les niveaux "5" et "9" deviendront "2" et "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vider cette collection conservera les signets et les placera tous au même niveau hiérarchique.
outlineLevels.Clear();
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


