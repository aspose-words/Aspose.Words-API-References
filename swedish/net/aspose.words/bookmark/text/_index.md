---
title: Bookmark.Text
second_title: Aspose.Words för .NET API Referens
description: Bookmark fast egendom. Hämtar eller ställer in texten innesluten i bokmärket.
type: docs
weight: 70
url: /sv/net/aspose.words/bookmark/text/
---
## Bookmark.Text property

Hämtar eller ställer in texten innesluten i bokmärket.

```csharp
public string Text { get; set; }
```

### Exempel

Visar hur du lägger till bokmärken och uppdaterar deras innehåll.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Skapa ett dokument med tre bokmärken och använd sedan en anpassad dokumentbesökarimplementering för att skriva ut innehållet.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Bokmärken kan nås i bokmärkessamlingen genom index eller namn, och deras namn kan uppdateras.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Skriv ut alla bokmärken igen för att se uppdaterade värden.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Skapa ett dokument med ett givet antal bokmärken.
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
/// Använd en iterator och en besökare för att skriva ut information om varje bokmärke i samlingen.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Skaffa varje bokmärke i samlingen för att acceptera en besökare som skriver ut dess innehåll.
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
/// Skriver ut innehållet i alla besökta bokmärken till konsolen.
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

### Se även

* class [Bookmark](../)
* namnutrymme [Aspose.Words](../../bookmark/)
* hopsättning [Aspose.Words](../../../)


