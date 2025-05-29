---
title: Bookmark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Ta enkelt bort bokmärken från ditt dokument samtidigt som du behåller texten inuti. Effektivisera din redigeringsprocess med vår effektiva metod för att ta bort bokmärken!
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
// 1 - Anrop av bokmärkets metod Ta bort:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Skicka bokmärket till samlingens Remove-metod:
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

// Texten som fanns inuti bokmärkena finns fortfarande kvar i dokumentet.
Assert.AreEqual(0, bookmarks.Count);
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
