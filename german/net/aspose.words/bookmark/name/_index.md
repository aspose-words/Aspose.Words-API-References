---
title: Bookmark.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Lesezeichen mühelos mit Bookmark Name. Legen Sie einfach Lesezeichennamen fest oder aktualisieren Sie diese für eine bessere Organisation und schnellen Zugriff.
type: docs
weight: 60
url: /de/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

Ruft den Namen des Lesezeichens ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Beachten Sie: Wenn Sie den Namen eines Lesezeichens in einen Namen ändern, der bereits im Dokument vorhanden ist, wird kein Fehler ausgegeben und beim Speichern des Dokuments wird nur das erste Lesezeichen gespeichert.

## Beispiele

Zeigt, wie ein Lesezeichen eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein gültiges Lesezeichen hat einen Namen, einen BookmarkStart- und einen BookmarkEnd-Knoten.
// Alle Leerzeichen in den Namen der Lesezeichen werden in Unterstriche umgewandelt, wenn wir das gespeicherte Dokument mit Microsoft Word öffnen.
// Wenn wir in Microsoft Word über Einfügen -> Links -> Lesezeichen den Namen des Lesezeichens markieren und auf "Gehe zu" drücken,
// Der Cursor springt zum Text zwischen den Knoten „BookmarkStart“ und „BookmarkEnd“.
builder.StartBookmark("My Bookmark");
builder.Write("Contents of MyBookmark.");
builder.EndBookmark("My Bookmark");

// In dieser Sammlung werden Lesezeichen gespeichert.
Assert.AreEqual("My Bookmark", doc.Range.Bookmarks[0].Name);

doc.Save(ArtifactsDir + "Bookmarks.Insert.docx");
```

Zeigt, wie Lesezeichen hinzugefügt und deren Inhalte aktualisiert werden.

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

    // Drucken Sie alle Lesezeichen erneut, um die aktualisierten Werte anzuzeigen.
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

    // Sorgen Sie dafür, dass jedes Lesezeichen in der Sammlung einen Besucher akzeptiert, der seinen Inhalt druckt.
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
/// Druckt den Inhalt jedes besuchten Lesezeichens auf der Konsole.
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

* class [Bookmark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
