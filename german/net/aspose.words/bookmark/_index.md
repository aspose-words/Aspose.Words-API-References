---
title: Class Bookmark
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Bookmark klas. Stellt ein einzelnes Lesezeichen dar.
type: docs
weight: 30
url: /de/net/aspose.words/bookmark/
---
## Bookmark class

Stellt ein einzelnes Lesezeichen dar.

```csharp
public class Bookmark
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Ruft den Knoten ab, der das Ende des Lesezeichens darstellt. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Ruft den Knoten ab, der den Anfang des Lesezeichens darstellt. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Ruft den nullbasierten Index der ersten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | gibt zurück **Stimmt** wenn dieses Lesezeichen ein Tabellenspalten-Lesezeichen ist. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Ruft den nullbasierten Index der letzten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Ruft den im Lesezeichen eingeschlossenen Text ab oder setzt ihn. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Entfernt das Lesezeichen aus dem Dokument. Entfernt keinen Text innerhalb des Lesezeichens. |

### Bemerkungen

`Bookmark` ist ein "Fassaden"-Objekt, das zwei Knoten kapselt[`BookmarkStart`](./bookmarkstart/) und[`BookmarkEnd`](./bookmarkend/) in einem Dokumentenbaum und ermöglicht es, mit einem Lesezeichen als einzelnes Objekt zu arbeiten.

### Beispiele

Zeigt, wie Lesezeichen hinzugefügt und deren Inhalt aktualisiert werden.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Erstellen Sie ein Dokument mit drei Lesezeichen und verwenden Sie dann eine benutzerdefinierte Dokumentbesucherimplementierung, um deren Inhalt zu drucken.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Auf Lesezeichen kann in der Lesezeichensammlung nach Index oder Name zugegriffen werden, und ihre Namen können aktualisiert werden.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Alle Lesezeichen erneut drucken, um aktualisierte Werte zu sehen.
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
/// Verwenden Sie einen Iterator und einen Besucher, um Informationen zu jedem Lesezeichen in der Sammlung zu drucken.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Lassen Sie jedes Lesezeichen in der Sammlung einen Besucher akzeptieren, der seinen Inhalt druckt.
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
/// Gibt den Inhalt jedes besuchten Lesezeichens auf der Konsole aus.
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


