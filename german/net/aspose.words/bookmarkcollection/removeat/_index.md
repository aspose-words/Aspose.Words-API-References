---
title: BookmarkCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Lesezeichen mühelos mit der RemoveAt-Methode – löschen Sie schnell jedes Lesezeichen anhand seines Indexes für eine optimierte Sammlung!
type: docs
weight: 60
url: /de/net/aspose.words/bookmarkcollection/removeat/
---
## BookmarkCollection.RemoveAt method

Entfernt ein Lesezeichen am angegebenen Index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index des zu entfernenden Lesezeichens. |

## Beispiele

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Fügen Sie fünf Lesezeichen mit Text innerhalb ihrer Grenzen ein.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Diese Sammlung speichert Lesezeichen.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Es gibt mehrere Möglichkeiten, Lesezeichen zu entfernen.
// 1 - Aufrufen der Remove-Methode des Lesezeichens:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 – Übergeben des Lesezeichens an die Remove-Methode der Sammlung:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Entfernen eines Lesezeichens aus der Sammlung nach Namen:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Entfernen eines Lesezeichens an einem Index in der Lesezeichensammlung:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Wir können die gesamte Lesezeichensammlung löschen.
bookmarks.Clear();

// Der Text, der sich in den Lesezeichen befand, ist weiterhin im Dokument vorhanden.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Siehe auch

* class [BookmarkCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
