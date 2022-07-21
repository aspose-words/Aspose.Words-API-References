---
title: BookmarkStart
second_title: Aspose.Words for .NET API Referansı
description: Bir Word belgesindeki yer işaretinin başlangıcını temsil eder.
type: docs
weight: 60
url: /tr/net/aspose.words/bookmarkstart/
---
## BookmarkStart class

Bir Word belgesindeki yer işaretinin başlangıcını temsil eder.

```csharp
public class BookmarkStart : Node
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [BookmarkStart](bookmarkstart)(DocumentBase, string) | Yeni bir örneğini başlatır[`BookmarkStart`](../bookmarkstart) sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bookmark](../../aspose.words/bookmarkstart/bookmark) { get; } | Bu yer iminin başlangıç ve bitişini kapsayan cephe nesnesini alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [Name](../../aspose.words/bookmarkstart/name) { get; set; } | Yer imi adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/bookmarkstart/nodetype) { get; } | İadeBookmarkStart . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkstart/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| override [GetText](../../aspose.words/bookmarkstart/gettext)() | Boş bir dize döndürür. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Bir Word belgesindeki eksiksiz bir yer imi, bir[`BookmarkStart`](../bookmarkstart) ve eşleşen[`BookmarkEnd`](../bookmarkend) aynı yer imi adıyla.

[`BookmarkStart`](../bookmarkstart) ve[`BookmarkEnd`](../bookmarkend) sadece yer iminin nerede başlayıp nerede bittiğini belirten bir document içindeki işaretlerdir.

Kullan[`Bookmark`](./bookmark) bookmark ile tek bir nesne olarak çalışmak için "cephe" olarak sınıflandırın.

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

* class [Node](../node)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
