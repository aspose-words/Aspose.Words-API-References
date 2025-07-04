---
title: Bookmark Class
linktitle: Bookmark
articleTitle: Bookmark
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Bookmark class, your solution for managing bookmarks efficiently in documents. Enhance your document editing experience today!
type: docs
weight: 220
url: /net/aspose.words/bookmark/
---
## Bookmark class

Represents a single bookmark.

To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/net/working-with-bookmarks/) documentation article.

```csharp
public class Bookmark
```

## Properties

| Name | Description |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Gets the node that represents the end of the bookmark. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Gets the node that represents the start of the bookmark. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | Returns `true` if this bookmark is a table column bookmark. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Gets or sets the name of the bookmark. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Gets or sets the text enclosed in the bookmark. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Removes the bookmark from the document. Does not remove text inside the bookmark. |

## Remarks

`Bookmark` is a "facade" object that encapsulates two nodes [`BookmarkStart`](./bookmarkstart/) and [`BookmarkEnd`](./bookmarkend/) in a document tree and allows to work with a bookmark as a single object.

## Examples

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
