---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: .NET için Aspose.Words
description: Belgelerinizdeki yer imlerini yönetmek, organizasyonu ve gezinmeyi geliştirmek için güçlü bir araç olan Aspose.Words.BookmarkCollection sınıfını keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Bir koleksiyon[`Bookmark`](../bookmark/) belirtilen aralıktaki yer imlerini temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yer İşaretleriyle Çalışma](https://docs.aspose.com/words/net/working-with-bookmarks/) belgeleme makalesi.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Koleksiyondaki yer imlerinin sayısını döndürür. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Belirtilen dizinde bir yer imi döndürür. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Bu koleksiyondan ve belgeden tüm yer imlerini kaldırır. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | Belirtilen yer imini belgeden kaldırır. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | Belirtilen ada sahip bir yer imini kaldırır. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | Belirtilen dizindeki bir yer işaretini kaldırır. |

## Örnekler

Yer imlerinin nasıl ekleneceğini ve içeriklerinin nasıl güncelleneceğini gösterir.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Üç yer imi içeren bir belge oluşturun, ardından içeriklerini yazdırmak için özel bir belge ziyaretçisi uygulaması kullanın.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Yer imlerine yer imi koleksiyonunda indeks veya isimle erişilebilir ve isimleri güncellenebilir.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Güncellenmiş değerleri görmek için tüm yer imlerini tekrar yazdır.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Belirtilen sayıda yer imi içeren bir belge oluşturun.
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
/// Koleksiyondaki her yer iminin bilgisini yazdırmak için bir yineleyici ve bir ziyaretçi kullanın.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Koleksiyondaki her yer iminin, içeriğini yazdıracak bir ziyaretçiyi kabul etmesini sağla.
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
/// Ziyaret edilen her yer iminin içeriğini konsola yazdırır.
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

### Ayrıca bakınız

* class [Bookmark](../bookmark/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
