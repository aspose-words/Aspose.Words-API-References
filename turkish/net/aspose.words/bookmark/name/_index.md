---
title: Bookmark.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Yer imlerinizi Bookmark Name ile zahmetsizce yönetin. Daha iyi organizasyon ve hızlı erişim için yer imi adlarınızı kolayca ayarlayın veya güncelleyin.
type: docs
weight: 60
url: /tr/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

Yer iminin adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

Bir yer iminin adını belgede zaten var olan bir adla değiştirirseniz, herhangi bir hata verilmeyeceğini ve belgeyi kaydettiğinizde yalnızca ilk yer imi saklanacağını unutmayın.

## Örnekler

Yer iminin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer iminin bir adı, bir BookmarkStart ve bir BookmarkEnd düğümü vardır.
// Kaydedilen belgeyi Microsoft Word ile açtığımızda yer imlerinin adlarındaki boşluklar alt çizgiye dönüştürülecektir.
// Microsoft Word'de Ekle -> Bağlantılar -> Yer İmi ile yer iminin adını vurgulayıp "Git"e basarsak,
// imleç BookmarkStart ve BookmarkEnd düğümleri arasında kalan metne atlayacaktır.
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

* class [Bookmark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
