---
title: Bookmark.Name
second_title: Aspose.Words for .NET API Referansı
description: Bookmark mülk. Yer iminin adını alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

Yer iminin adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

### Notlar

Bir yer iminin adını belgede zaten var olan bir adla değiştirirseniz, hata verilmeyeceğini ve belgeyi kaydettiğinizde yalnızca ilk yer iminin saklanacağını unutmayın.

### Örnekler

Yer iminin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer işaretinin bir adı, bir BookmarkStart ve bir BookmarkEnd düğümü vardır.
// Kaydedilen belgeyi Microsoft Word ile açarsak, yer imlerinin adlarındaki boşluklar alt çizgiye dönüştürülür. 
// Yer iminin adını Microsoft Word'de Ekle -> Bağlantılar -> İşaretleyin ve "Git"e basın,
// imleç BookmarkStart ve BookmarkEnd düğümleri arasında yer alan metne atlayacaktır.
builder.StartBookmark("My Bookmark");
builder.Write("Contents of MyBookmark.");
builder.EndBookmark("My Bookmark");

// Yer imleri bu koleksiyonda saklanır.
Assert.AreEqual("My Bookmark", doc.Range.Bookmarks[0].Name);

doc.Save(ArtifactsDir + "Bookmarks.Insert.docx");
```

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

* class [Bookmark](../)
* ad alanı [Aspose.Words](../../bookmark/)
* toplantı [Aspose.Words](../../../)


