---
title: Bookmark Class
linktitle: Bookmark
articleTitle: Bookmark
second_title: .NET için Aspose.Words
description: Belgelerde yer imlerini etkili bir şekilde yönetmeniz için çözümünüz olan Aspose.Words.Bookmark sınıfını keşfedin. Belge düzenleme deneyiminizi bugün geliştirin!
type: docs
weight: 230
url: /tr/net/aspose.words/bookmark/
---
## Bookmark class

Tek bir yer imini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yer İşaretleriyle Çalışma](https://docs.aspose.com/words/net/working-with-bookmarks/) belgeleme makalesi.

```csharp
public class Bookmark
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | Yer iminin sonunu temsil eden düğümü alır. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | Yer iminin başlangıcını temsil eden düğümü alır. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | Yer imiyle ilişkili tablo sütun aralığının ilk sütununun sıfır tabanlı dizinini alır. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | Geri Döndürür`doğru` eğer bu yer imi bir tablo sütun yer imi ise. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | Yer imiyle ilişkili tablo sütun aralığının son sütununun sıfır tabanlı dizinini alır. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | Yer iminin adını alır veya ayarlar. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | Yer imine eklenen metni alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | Yer imini belgeden kaldırır. Yer imi içindeki metni kaldırmaz. |

## Notlar

`Bookmark` iki düğümü kapsayan bir "cephe" nesnesidir[`BookmarkStart`](./bookmarkstart/) ve[`BookmarkEnd`](./bookmarkend/) Bir belge ağacında yer alır ve yer imleriyle tek bir nesne olarak çalışmaya olanak tanır.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
