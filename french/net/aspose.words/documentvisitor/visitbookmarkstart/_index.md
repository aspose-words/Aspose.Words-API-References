---
title: DocumentVisitor.VisitBookmarkStart
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentVisitor méthode. Appelé lorsquun début de signet est rencontré dans le document.
type: docs
weight: 50
url: /fr/net/aspose.words/documentvisitor/visitbookmarkstart/
---
## DocumentVisitor.VisitBookmarkStart method

Appelé lorsqu'un début de signet est rencontré dans le document.

```csharp
public virtual VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| bookmarkStart | BookmarkStart | L'objet qui est visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment continuer l’énumération.

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

* enum [VisitorAction](../../visitoraction/)
* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../documentvisitor/)
* Assemblée [Aspose.Words](../../../)


