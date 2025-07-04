---
title: BookmarkCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: Effortlessly clear all bookmarks from your document with the BookmarkCollection Clear method. Streamline your workflow and enhance organization today!
type: docs
weight: 30
url: /net/aspose.words/bookmarkcollection/clear/
---
## BookmarkCollection.Clear method

Removes all bookmarks from this collection and from the document.

```csharp
public void Clear()
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

Assert.That(bookmarks.Count, Is.EqualTo(5));

// There are several ways of removing bookmarks.
// 1 -  Calling the bookmark's Remove method:
bookmarks["MyBookmark_1"].Remove();

Assert.That(bookmarks.Any(b => b.Name == "MyBookmark_1"), Is.False);

// 2 -  Passing the bookmark to the collection's Remove method:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.That(bookmarks.Any(b => b.Name == "MyBookmark_2"), Is.False);

// 3 -  Removing a bookmark from the collection by name:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.That(bookmarks.Any(b => b.Name == "MyBookmark_3"), Is.False);

// 4 -  Removing a bookmark at an index in the bookmark collection:
doc.Range.Bookmarks.RemoveAt(0);

Assert.That(bookmarks.Any(b => b.Name == "MyBookmark_4"), Is.False);

// We can clear the entire bookmark collection.
bookmarks.Clear();

// The text that was inside the bookmarks is still present in the document.
Assert.That(bookmarks.Count, Is.EqualTo(0));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5."));
```

### See Also

* class [BookmarkCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
