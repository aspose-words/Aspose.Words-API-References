---
title: Class Bookmark
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Bookmark classe. Représente un seul signet.
type: docs
weight: 40
url: /fr/net/aspose.words/bookmark/
---
## Bookmark class

Représente un seul signet.

Pour en savoir plus, visitez le[Travailler avec des signets](https://docs.aspose.com/words/net/working-with-bookmarks/) article documentaire.

```csharp
public class Bookmark
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Obtient le nœud qui représente la fin du signet. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Obtient le nœud qui représente le début du signet. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Obtient l'index de base zéro de la première colonne de la plage de colonnes du tableau associée au signet. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | Retours`vrai` si ce signet est un signet de colonne de tableau. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Obtient l'index de base zéro de la dernière colonne de la plage de colonnes du tableau associée au signet. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Obtient ou définit le nom du signet. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Obtient ou définit le texte inclus dans le signet. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Supprime le signet du document. Ne supprime pas le texte à l'intérieur du signet. |

### Remarques

`Bookmark` est un objet "façade" qui encapsule deux nœuds[`BookmarkStart`](./bookmarkstart/) et[`BookmarkEnd`](./bookmarkend/) dans une arborescence de documents et permet de travailler avec un signet comme un objet unique.

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


