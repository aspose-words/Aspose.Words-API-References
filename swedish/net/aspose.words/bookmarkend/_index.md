---
title: BookmarkEnd Class
linktitle: BookmarkEnd
articleTitle: BookmarkEnd
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.BookmarkEnd, som effektivt hanterar bokmärkesslut i Word-dokument och förbättrar din dokumentredigeringsupplevelse.
type: docs
weight: 250
url: /sv/net/aspose.words/bookmarkend/
---
## BookmarkEnd class

Representerar slutet på ett bokmärke i ett Word-dokument.

För att lära dig mer, besök[Arbeta med bokmärken](https://docs.aspose.com/words/net/working-with-bookmarks/) dokumentationsartikel.

```csharp
public class BookmarkEnd : Node
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [BookmarkEnd](bookmarkend/)(*[DocumentBase](../documentbase/), string*) | Initierar en ny instans av`BookmarkEnd` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returer`sann` om denna nod kan innehålla andra noder. |
| [Name](../../aspose.words/bookmarkend/name/) { get; set; } | Hämtar eller ställer in bokmärkets namn. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/bookmarkend/nodetype/) { get; } | ReturerBookmarkEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Ett komplett bokmärke i ett Word-dokument består av en[`BookmarkStart`](../bookmarkstart/) och en matchande`BookmarkEnd` med samma bokmärkesnamn.

[`BookmarkStart`](../bookmarkstart/) och`BookmarkEnd` är bara markörer inuti ett document som anger var bokmärket börjar och slutar.

Använd[`Bookmark`](../bookmark/) klassen som en "fasad" för att fungera med ett bookmark som ett enda objekt.

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

* class [Node](../node/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
