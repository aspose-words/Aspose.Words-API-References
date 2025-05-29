---
title: BookmarkCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BookmarkCollection Count, qui renvoie efficacement le nombre total de signets, améliorant ainsi vos capacités de gestion des données.
type: docs
weight: 10
url: /fr/net/aspose.words/bookmarkcollection/count/
---
## BookmarkCollection.Count property

Renvoie le nombre de signets dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Montre comment supprimer les signets d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer cinq signets avec du texte à l'intérieur de leurs limites.
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

// 3 - Suppression d'un signet de la collection par nom :
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Suppression d'un signet à un index dans la collection de signets :
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Nous pouvons effacer toute la collection de signets.
bookmarks.Clear();

// Le texte qui se trouvait à l'intérieur des signets est toujours présent dans le document.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Voir également

* class [BookmarkCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
