---
title: BookmarkCollection.Remove
second_title: Référence de l'API Aspose.Words pour .NET
description: BookmarkCollection méthode. Supprime le signet spécifié du document.
type: docs
weight: 50
url: /fr/net/aspose.words/bookmarkcollection/remove/
---
## Remove(Bookmark) {#remove}

Supprime le signet spécifié du document.

```csharp
public void Remove(Bookmark bookmark)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmark | Bookmark | Marque-page à supprimer. |

### Exemples

Montre comment supprimer des signets d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère cinq signets avec du texte à l'intérieur de leurs limites.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Cette collection stocke les signets.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Il existe plusieurs façons de supprimer des signets.
// 1 - Appel de la méthode Remove du signet :
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Passage du signet à la méthode Remove de la collection :
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Suppression d'un signet de la collection par son nom :
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Suppression d'un signet à un index de la collection de signets :
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Nous pouvons effacer toute la collection de signets.
bookmarks.Clear();

// Le texte qui était à l'intérieur des signets est toujours présent dans le document.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Voir également

* class [Bookmark](../../bookmark/)
* class [BookmarkCollection](../)
* espace de noms [Aspose.Words](../../bookmarkcollection/)
* Assemblée [Aspose.Words](../../../)

---

## Remove(string) {#remove_1}

Supprime un signet avec le nom spécifié.

```csharp
public void Remove(string bookmarkName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmarkName | String | Le nom insensible à la casse du signet à supprimer. |

### Exemples

Montre comment supprimer des signets d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère cinq signets avec du texte à l'intérieur de leurs limites.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Cette collection stocke les signets.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Il existe plusieurs façons de supprimer des signets.
// 1 - Appel de la méthode Remove du signet :
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Passage du signet à la méthode Remove de la collection :
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Suppression d'un signet de la collection par son nom :
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Suppression d'un signet à un index de la collection de signets :
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Nous pouvons effacer toute la collection de signets.
bookmarks.Clear();

// Le texte qui était à l'intérieur des signets est toujours présent dans le document.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Voir également

* class [BookmarkCollection](../)
* espace de noms [Aspose.Words](../../bookmarkcollection/)
* Assemblée [Aspose.Words](../../../)


