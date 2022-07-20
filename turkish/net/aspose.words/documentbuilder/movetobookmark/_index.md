---
title: MoveToBookmark
second_title: Aspose.Words for .NET API Referansı
description: İmleci bir yer işaretine taşır.
type: docs
weight: 470
url: /tr/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

İmleci bir yer işaretine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |

### Geri dönüş değeri

Yer imi bulunduysa doğrudur; aksi halde yanlış.

### Notlar

İmleci, belirtilen ada sahip yer iminin başlangıcından hemen sonraki bir konuma taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa, false is döndürülür ve imleç hareket etmez.

Yeni metin eklemek, yer iminin mevcut metnini değiştirmez.

Belgedeki bazı yer imlerinin form alanlarına atandığını unutmayın. Böyle bir yer imine geçmek ve oraya metin eklemek, metni form alanı koduna ekler. Bu, form alanını geçersiz kılmasa da, eklenen metni, alan kodunun bir parçası olduğu için görünmeyecektir.

### Örnekler

Bir belge oluşturucunun imlecinin bir belgedeki farklı düğümlere nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer imi oluşturun, bir yer imi başlangıç düğümü tarafından çevrelenen düğümlerden oluşan bir varlık,
 // ve bir yer imi bitiş düğümü.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Belge oluşturucunun imleci her zaman onunla son eklediğimiz düğümün önündedir.
// Oluşturucunun imleci belgenin sonundaysa, mevcut düğümü boş olur.
// Önceki düğüm, en son eklediğimiz yer imi bitiş düğümüdür.
// Oluşturucu ile yeni düğümler eklemek onları son düğüme ekleyecektir.
Assert.Null(builder.CurrentNode);

// Oluşturucu ile belgenin farklı bir bölümünü düzenlemek istersek,
// imlecini düzenlemek istediğimiz düğüme getirmemiz gerekecek.
builder.MoveToBookmark("MyBookmark");

// Onu bir yer imine taşımak, onu yer imi başlangıç ve bitiş düğümleri içindeki ilk düğüme, ekteki çalıştırmaya taşır.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// İmleci bu şekilde tek bir düğüme de taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Bir belgenin başına/sonuna gitmek için belirli yöntemler kullanabiliriz.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Ayrıca bakınız

* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

İmleci daha hassas bir şekilde bir yer işaretine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |
| isStart | Boolean | Doğru olduğunda, imleci yer iminin başına taşır. Yanlış olduğunda, imleci yer iminin sonuna taşır. |
| isAfter | Boolean | true olduğunda, imleci bookmark başlangıç veya bitiş konumundan sonra olacak şekilde hareket ettirir. Yanlış olduğunda, imleci bookmark başlangıç veya bitiş konumundan önce olacak şekilde hareket ettirir. |

### Geri dönüş değeri

Yer imi bulunduysa doğrudur; aksi halde yanlış.

### Notlar

İmleci, yer iminin başlangıcından veya sonundan önceki veya sonraki bir konuma taşır.

İstenen konum satır içi düzeyde değilse bir sonraki paragrafa geçer.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa, false is döndürülür ve imleç hareket etmez.

### Örnekler

Bir belge oluşturucunun düğüm ekleme noktası imlecinin bir yer işaretine nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer imi, bir BookmarkStart düğümünden, bir BookmarkEnd düğümünden oluşur.
// yer imi adını daha sonra bir yerde eşleştirme ve bu düğümlerin içerdiği içerikler.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Bir belge oluşturucunun imlecini bir yer işaretine taşımanın 4 yolu vardır.
// BookmarkStart ve BookmarkEnd düğümleri arasındaysak, imleç yer iminin içinde olacaktır.
// Bu, oluşturucu tarafından eklenen herhangi bir metnin yer iminin bir parçası olacağı anlamına gelir.
// 1 - Yer işaretinin dışında, BookmarkStart düğümünün önünde:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Yer işaretinin içinde, BookmarkStart düğümünden hemen sonra:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - Yer işaretinin içinde, BookmarkEnd düğümünün hemen önünde:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Yer işaretinin dışında, BookmarkEnd düğümünden sonra:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
