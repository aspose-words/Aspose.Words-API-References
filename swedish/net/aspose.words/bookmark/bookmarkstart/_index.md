---
title: Bookmark.BookmarkStart
linktitle: BookmarkStart
articleTitle: BookmarkStart
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BookmarkStart för att enkelt komma åt noden som markerar ditt bokmärkes början, vilket förbättrar navigeringen och effektiviteten i ditt projekt.
type: docs
weight: 20
url: /sv/net/aspose.words/bookmark/bookmarkstart/
---
## Bookmark.BookmarkStart property

Hämtar noden som representerar början av bokmärket.

```csharp
public BookmarkStart BookmarkStart { get; }
```

## Exempel

Visar hur man lägger till bokmärken och uppdaterar deras innehåll.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Skapa ett dokument med tre bokmärken och använd sedan en anpassad dokumentbesökarimplementering för att skriva ut innehållet.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Bokmärken kan nås i bokmärkessamlingen via index eller namn, och deras namn kan uppdateras.
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

    // Få varje bokmärke i samlingen att acceptera en besökare som skriver ut dess innehåll.
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
/// Skriver ut innehållet i varje besökt bokmärke till konsolen.
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

* class [BookmarkStart](../../bookmarkstart/)
* class [Bookmark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
