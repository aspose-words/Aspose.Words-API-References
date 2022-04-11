---
title: "Item"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 60
url: /net/aspose.words/bookmarkcollection/item/
---
## BookmarkCollection indexer (1 of 2)

Returns a bookmark at the specified index.

```csharp
public Bookmark this[int index] { get; }
```

| Parameter | Type | Description |
| --- | --- | --- |
| index |  | An index into the collection. |

### Remarks

The index is zero-based.Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.If index is greater than or equal to the number of items in the list, this returns a null reference.If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

### Examples

Shows how to add bookmarks and update their contents.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Print all bookmarks again to see updated values.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Create a document with a given number of bookmarks.
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
/// Use an iterator and a visitor to print info of every bookmark in the collection.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Get each bookmark in the collection to accept a visitor that will print its contents.
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
/// Prints contents of every visited bookmark to the console.
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

### See Also

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* namespace [Aspose.Words](../../bookmarkcollection)
* assembly [Aspose.Words](../../../)

---

## BookmarkCollection indexer (2 of 2)

Returns a bookmark by name.

```csharp
public Bookmark this[string bookmarkName] { get; }
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName |  | Case-insensitive name of the bookmark. |

### Remarks

Returns null if the bookmark with the specified name cannot be found.

### Examples

Shows how to add bookmarks and update their contents.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Print all bookmarks again to see updated values.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Create a document with a given number of bookmarks.
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
/// Use an iterator and a visitor to print info of every bookmark in the collection.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Get each bookmark in the collection to accept a visitor that will print its contents.
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
/// Prints contents of every visited bookmark to the console.
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

### See Also

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* namespace [Aspose.Words](../../bookmarkcollection)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
