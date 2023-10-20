---
title: Bookmark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Bookmark Remove metod. Tar bort bokmärket från dokumentet. Tar inte bort text inuti bokmärket i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/bookmark/remove/
---
## Bookmark.Remove method

Tar bort bokmärket från dokumentet. Tar inte bort text inuti bokmärket.

```csharp
public void Remove()
```

## Exempel

Visar hur man tar bort bokmärken från ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga fem bokmärken med text innanför deras gränser.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Den här samlingen lagrar bokmärken.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Det finns flera sätt att ta bort bokmärken.
// 1 - Anropar bokmärkets borttagningsmetod:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Skicka bokmärket till samlingens borttagningsmetod:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Ta bort ett bokmärke från samlingen efter namn:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Ta bort ett bokmärke i ett index i bokmärkessamlingen:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Vi kan rensa hela bokmärkessamlingen.
bookmarks.Clear();

// Texten som fanns i bokmärkena finns fortfarande kvar i dokumentet.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Se även

* class [Bookmark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
