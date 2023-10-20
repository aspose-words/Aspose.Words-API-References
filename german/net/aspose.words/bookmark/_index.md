---
title: Bookmark Class
linktitle: Bookmark
articleTitle: Bookmark
second_title: Aspose.Words für .NET
description: Aspose.Words.Bookmark klas. Stellt ein einzelnes Lesezeichen dar in C#.
type: docs
weight: 40
url: /de/net/aspose.words/bookmark/
---
## Bookmark class

Stellt ein einzelnes Lesezeichen dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Lesezeichen](https://docs.aspose.com/words/net/working-with-bookmarks/) Dokumentationsartikel.

```csharp
public class Bookmark
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Ruft den Knoten ab, der das Ende des Lesezeichens darstellt. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Ruft den Knoten ab, der den Anfang des Lesezeichens darstellt. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Ruft den nullbasierten Index der ersten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | Gibt zurück`WAHR` wenn dieses Lesezeichen ein Tabellenspalten-Lesezeichen ist. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Ruft den nullbasierten Index der letzten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Ruft den im Lesezeichen eingeschlossenen Text ab oder legt diesen fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Entfernt das Lesezeichen aus dem Dokument. Entfernt keinen Text im Lesezeichen. |

## Bemerkungen

`Bookmark` ist ein „Fassaden“-Objekt, das zwei Knoten kapselt[`BookmarkStart`](./bookmarkstart/) und[`BookmarkEnd`](./bookmarkend/) in einem Dokumentbaum und ermöglicht die Arbeit mit einem Lesezeichen als einzelnes Objekt.

## Beispiele

Zeigt, wie Sie Lesezeichen hinzufügen und deren Inhalte aktualisieren.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Erstellen Sie ein Dokument mit drei Lesezeichen und verwenden Sie dann eine benutzerdefinierte Dokumentbesucherimplementierung, um deren Inhalte zu drucken.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Auf Lesezeichen kann in der Lesezeichensammlung nach Index oder Name zugegriffen werden, und ihre Namen können aktualisiert werden.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Alle Lesezeichen erneut drucken, um aktualisierte Werte anzuzeigen.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Erstellen Sie ein Dokument mit einer bestimmten Anzahl von Lesezeichen.
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
/// Verwenden Sie einen Iterator und einen Besucher, um Informationen zu jedem Lesezeichen in der Sammlung auszudrucken.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Jedes Lesezeichen in der Sammlung dazu bringen, einen Besucher zu akzeptieren, der seinen Inhalt druckt.
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
/// Gibt den Inhalt jedes besuchten Lesezeichens an die Konsole aus.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
