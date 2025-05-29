---
title: Bookmark.BookmarkEnd
linktitle: BookmarkEnd
articleTitle: BookmarkEnd
second_title: Aspose.Words per .NET
description: Scopri la proprietà BookmarkEnd e accedi facilmente al nodo che segna la fine del tuo segnalibro per una navigazione e una gestione efficienti dei documenti.
type: docs
weight: 10
url: /it/net/aspose.words/bookmark/bookmarkend/
---
## Bookmark.BookmarkEnd property

Ottiene il nodo che rappresenta la fine del segnalibro.

```csharp
public BookmarkEnd BookmarkEnd { get; }
```

## Esempi

Mostra come aggiungere segnalibri e aggiornarne il contenuto.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Crea un documento con tre segnalibri, quindi utilizza un'implementazione personalizzata del visitatore del documento per stamparne il contenuto.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // È possibile accedere ai segnalibri nella raccolta dei segnalibri tramite indice o nome e i loro nomi possono essere aggiornati.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Stampa nuovamente tutti i segnalibri per visualizzare i valori aggiornati.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crea un documento con un dato numero di segnalibri.
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

    // Fai in modo che ogni segnalibro nella raccolta accetti un visitatore che ne stamperà il contenuto.
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

* class [BookmarkEnd](../../bookmarkend/)
* class [Bookmark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
