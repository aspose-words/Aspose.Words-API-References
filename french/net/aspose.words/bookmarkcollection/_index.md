---
title: Class BookmarkCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.BookmarkCollection classe. Une collection deBookmark objets qui représentent les signets dans la plage spécifiée.
type: docs
weight: 50
url: /fr/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Une collection de[`Bookmark`](../bookmark/) objets qui représentent les signets dans la plage spécifiée.

Pour en savoir plus, visitez le[Travailler avec des signets](https://docs.aspose.com/words/net/working-with-bookmarks/) article documentaire.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Renvoie le nombre de signets dans la collection. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Renvoie un signet à l'index spécifié. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Supprime tous les signets de cette collection et du document. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(Bookmark) | Supprime le signet spécifié du document. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(string) | Supprime un signet avec le nom spécifié. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(int) | Supprime un signet à l'index spécifié. |

### Exemples

Montre comment ajouter des signets et mettre à jour leur contenu.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Créez un document avec trois signets, puis utilisez une implémentation de visiteur de document personnalisée pour imprimer leur contenu.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Les signets sont accessibles dans la collection de signets par index ou par nom, et leurs noms peuvent être mis à jour.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Imprimez à nouveau tous les signets pour voir les valeurs mises à jour.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crée un document avec un nombre donné de signets.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Utilisez un itérateur et un visiteur pour imprimer les informations de chaque signet de la collection.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Demande à chaque signet de la collection d'accepter un visiteur qui imprimera son contenu.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Imprime le contenu de chaque signet visité sur la console.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Voir également

* class [Bookmark](../bookmark/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


