---
title: BookmarkCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Veri yönetimi yeteneklerinizi geliştirerek, toplam yer imi sayısını verimli bir şekilde döndüren BookmarkCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/bookmarkcollection/count/
---
## BookmarkCollection.Count property

Koleksiyondaki yer imlerinin sayısını döndürür.

```csharp
public int Count { get; }
```

## Örnekler

Bir belgeden yer imlerinin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sınırları içerisinde metin bulunan beş yer imi ekleyin.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Bu koleksiyon yer imlerini depolar.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Yer imlerini kaldırmanın birkaç yolu vardır.
// 1 - Yer iminin Remove metodunun çağrılması:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Yer imini koleksiyonun Remove metoduna geçirmek:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Koleksiyondan ismine göre yer imini kaldırma:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Yer imi koleksiyonundaki bir dizindeki yer imini kaldırma:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Tüm yer imi koleksiyonunu temizleyebiliriz.
bookmarks.Clear();

// Yer imlerinin içindeki metin hala belgede mevcuttur.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [BookmarkCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
