---
title: Bookmark Class
linktitle: Bookmark
articleTitle: Bookmark
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Bookmark, la soluzione ideale per gestire in modo efficiente i segnalibri nei documenti. Migliora la tua esperienza di editing dei documenti oggi stesso!
type: docs
weight: 230
url: /it/net/aspose.words/bookmark/
---
## Bookmark class

Rappresenta un singolo segnalibro.

Per saperne di più, visita il[Lavorare con i segnalibri](https://docs.aspose.com/words/net/working-with-bookmarks/) articolo di documentazione.

```csharp
public class Bookmark
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Ottiene il nodo che rappresenta la fine del segnalibro. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Ottiene il nodo che rappresenta l'inizio del segnalibro. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Ottiene l'indice basato su zero della prima colonna dell'intervallo di colonne della tabella associato al segnalibro. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | Restituisce`VERO` se questo segnalibro è un segnalibro di colonna di tabella. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Ottiene l'indice basato su zero dell'ultima colonna dell'intervallo di colonne della tabella associato al segnalibro. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Ottiene o imposta il nome del segnalibro. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Ottiene o imposta il testo racchiuso nel segnalibro. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Rimuove il segnalibro dal documento. Non rimuove il testo all'interno del segnalibro. |

## Osservazioni

`Bookmark` è un oggetto "facciata" che incapsula due nodi[`BookmarkStart`](./bookmarkstart/) e[`BookmarkEnd`](./bookmarkend/) in un albero di documenti e consente di lavorare con un segnalibro come un singolo oggetto.

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
