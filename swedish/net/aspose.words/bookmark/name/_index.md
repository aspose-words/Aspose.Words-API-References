---
title: Bookmark.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Hantera dina bokmärken enkelt med Bokmärkesnamn. Ställ enkelt in eller uppdatera dina bokmärkesnamn för bättre organisation och snabb åtkomst.
type: docs
weight: 60
url: /sv/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

Hämtar eller anger namnet på bokmärket.

```csharp
public string Name { get; set; }
```

## Anmärkningar

Observera att om du ändrar namnet på ett bokmärke till ett namn som redan finns i dokumentet, kommer inget felmeddelande att visas och endast det första bokmärket kommer att lagras när du sparar dokumentet.

## Exempel

Visar hur man lägger till ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett giltigt bokmärke har ett namn, en BookmarkStart och en BookmarkEnd-nod.
// Alla blanksteg i namnen på bokmärken konverteras till understreck om vi öppnar det sparade dokumentet med Microsoft Word.
// Om vi markerar bokmärkets namn i Microsoft Word via Infoga -> Länkar -> Bokmärke och trycker på "Gå till",
// markören hoppar till texten som finns mellan noderna BookmarkStart och BookmarkEnd.
builder.StartBookmark("My Bookmark");
builder.Write("Contents of MyBookmark.");
builder.EndBookmark("My Bookmark");

// Bokmärken lagras i den här samlingen.
Assert.AreEqual("My Bookmark", doc.Range.Bookmarks[0].Name);

doc.Save(ArtifactsDir + "Bookmarks.Insert.docx");
```

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

* class [Bookmark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
