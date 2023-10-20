---
title: BookmarkCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: BookmarkCollection Remove yöntem. Belirtilen yer imini belgeden kaldırır C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/bookmarkcollection/remove/
---
## Remove(*[Bookmark](../../bookmark/)*) {#remove}

Belirtilen yer imini belgeden kaldırır.

```csharp
public void Remove(Bookmark bookmark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmark | Bookmark | Kaldırılacak yer işareti. |

## Örnekler

Yer işaretlerinin bir belgeden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sınırları içinde metin bulunan beş yer imi ekleyin.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Bu koleksiyon yer imlerini saklar.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Yer imlerini kaldırmanın birkaç yolu vardır.
// 1 - Yer iminin Kaldır yöntemini çağırmak:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Yer işaretini koleksiyonun Remove yöntemine geçirme:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Koleksiyondan bir yer imini ada göre kaldırmak:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Yer imi koleksiyonundaki bir dizindeki yer işaretini kaldırma:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Yer imi koleksiyonunun tamamını temizleyebiliriz.
bookmarks.Clear();

// Yer imlerinin içindeki metin hâlâ belgede mevcut.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Bookmark](../../bookmark/)
* class [BookmarkCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Remove(*string*) {#remove_1}

Belirtilen ada sahip bir yer imini kaldırır.

```csharp
public void Remove(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Kaldırılacak yer işaretinin büyük/küçük harfe duyarlı olmayan adı. |

## Örnekler

Yer işaretlerinin bir belgeden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sınırları içinde metin bulunan beş yer imi ekleyin.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Bu koleksiyon yer imlerini saklar.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Yer imlerini kaldırmanın birkaç yolu vardır.
// 1 - Yer iminin Kaldır yöntemini çağırmak:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Yer işaretini koleksiyonun Remove yöntemine geçirme:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Koleksiyondan bir yer imini ada göre kaldırmak:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Yer imi koleksiyonundaki bir dizindeki yer işaretini kaldırma:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Yer imi koleksiyonunun tamamını temizleyebiliriz.
bookmarks.Clear();

// Yer imlerinin içindeki metin hâlâ belgede mevcut.
Assert.That(bookmarks, Is.Empty);
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
