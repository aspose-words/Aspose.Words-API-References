---
title: Bookmark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Easily remove bookmarks from your document while preserving the text inside. Streamline your editing process with our efficient Bookmark Remove method!
type: docs
weight: 80
url: /net/aspose.words/bookmark/remove/
---
## Bookmark.Remove method

Removes the bookmark from the document. Does not remove text inside the bookmark.

```csharp
public void Remove()
```

## Examples

Shows how to remove bookmarks from a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert five bookmarks with text inside their boundaries.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// This collection stores bookmarks.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// There are several ways of removing bookmarks.
// 1 -  Calling the bookmark's Remove method:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 -  Passing the bookmark to the collection's Remove method:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 -  Removing a bookmark from the collection by name:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 -  Removing a bookmark at an index in the bookmark collection:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// We can clear the entire bookmark collection.
bookmarks.Clear();

// The text that was inside the bookmarks is still present in the document.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### See Also

* class [Bookmark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
