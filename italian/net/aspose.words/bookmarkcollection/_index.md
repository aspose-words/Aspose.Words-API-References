---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.BookmarkCollection classe. Una raccolta diBookmark oggetti che rappresentano i segnalibri nellintervallo specificato in C#.
type: docs
weight: 50
url: /it/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Una raccolta di[`Bookmark`](../bookmark/) oggetti che rappresentano i segnalibri nell'intervallo specificato.

Per saperne di più, visita il[Lavorare con i segnalibri](https://docs.aspose.com/words/net/working-with-bookmarks/) articolo di documentazione.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Restituisce il numero di segnalibri nella raccolta. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Restituisce un segnalibro all'indice specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Rimuove tutti i segnalibri da questa raccolta e dal documento. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | Rimuove il segnalibro specificato dal documento. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | Rimuove un segnalibro con il nome specificato. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | Rimuove un segnalibro all'indice specificato. |

## Esempi

Mostra come aggiungere segnalibri e aggiornarne i contenuti.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Crea un documento con tre segnalibri, quindi utilizza un'implementazione personalizzata del visitatore del documento per stamparne il contenuto.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // È possibile accedere ai segnalibri nella raccolta di segnalibri tramite indice o nome e i relativi nomi possono essere aggiornati.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Stampa di nuovo tutti i segnalibri per vedere i valori aggiornati.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crea un documento con un determinato numero di segnalibri.
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
/// Utilizza un iteratore e un visitatore per stampare le informazioni di ogni segnalibro nella raccolta.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Fa in modo che ogni segnalibro nella raccolta accetti un visitatore che ne stamperà il contenuto.
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
/// Stampa sulla console il contenuto di ogni segnalibro visitato.
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

### Guarda anche

* class [Bookmark](../bookmark/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
