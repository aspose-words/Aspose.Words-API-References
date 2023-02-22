---
title: BookmarkEnd.BookmarkEnd
second_title: Aspose.Words for .NET API Referansı
description: BookmarkEnd inşaatçı. Yeni bir örneğini başlatırBookmarkEnd sınıf.
type: docs
weight: 10
url: /tr/net/aspose.words/bookmarkend/bookmarkend/
---
## BookmarkEnd constructor

Yeni bir örneğini başlatır[`BookmarkEnd`](../) sınıf.

```csharp
public BookmarkEnd(DocumentBase doc, string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| name | String | Yer iminin adı. Boş olamaz. |

### Örnekler

Yer imlerinin nasıl ekleneceğini ve içeriklerinin nasıl güncelleneceğini gösterir.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Üç yer imi içeren bir belge oluşturun, ardından içeriklerini yazdırmak için özel bir belge ziyaretçi uygulaması kullanın.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Yer imi koleksiyonundaki yer imlerine dizin veya isme göre erişilebilir ve adları güncellenebilir.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Güncellenen değerleri görmek için tüm yer imlerini yeniden yazdırın.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Belirli sayıda yer imi içeren bir belge oluşturun.
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
/// Koleksiyondaki her yer iminin bilgilerini yazdırmak için bir yineleyici ve bir ziyaretçi kullanın.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // İçeriğini yazdıracak bir ziyaretçiyi kabul etmek için koleksiyondaki her yer işaretini alın.
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

* class [DocumentBase](../../documentbase/)
* class [BookmarkEnd](../)
* ad alanı [Aspose.Words](../../bookmarkend/)
* toplantı [Aspose.Words](../../../)


