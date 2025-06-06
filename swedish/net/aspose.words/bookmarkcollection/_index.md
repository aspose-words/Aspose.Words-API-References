---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.BookmarkCollection, ett kraftfullt verktyg för att hantera bokmärken i dina dokument, förbättra organisation och navigering.
type: docs
weight: 240
url: /sv/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

En samling av[`Bookmark`](../bookmark/) objekt som representerar bokmärkena i det angivna området.

För att lära dig mer, besök[Arbeta med bokmärken](https://docs.aspose.com/words/net/working-with-bookmarks/) dokumentationsartikel.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Returnerar antalet bokmärken i samlingen. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Returnerar ett bokmärke vid det angivna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Tar bort alla bokmärken från den här samlingen och från dokumentet. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | Tar bort det angivna bokmärket från dokumentet. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | Tar bort ett bokmärke med det angivna namnet. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | Tar bort ett bokmärke vid det angivna indexet. |

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

* class [Bookmark](../bookmark/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
