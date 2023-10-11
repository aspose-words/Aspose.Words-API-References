---
title: Class BookmarkCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.BookmarkCollection klas. Eine Sammlung vonBookmark Objekte die die Lesezeichen im angegebenen Bereich darstellen.
type: docs
weight: 50
url: /de/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Eine Sammlung von[`Bookmark`](../bookmark/) Objekte, die die Lesezeichen im angegebenen Bereich darstellen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Lesezeichen](https://docs.aspose.com/words/net/working-with-bookmarks/) Dokumentationsartikel.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Gibt die Anzahl der Lesezeichen in der Sammlung zurück. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Gibt ein Lesezeichen am angegebenen Index zurück. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Entfernt alle Lesezeichen aus dieser Sammlung und aus dem Dokument. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(Bookmark) | Entfernt das angegebene Lesezeichen aus dem Dokument. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(string) | Entfernt ein Lesezeichen mit dem angegebenen Namen. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(int) | Entfernt ein Lesezeichen am angegebenen Index. |

### Beispiele

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

* class [Bookmark](../bookmark/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


