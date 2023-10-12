---
title: DocumentBuilder.MoveToBookmark
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci bir yer imine taşır.
type: docs
weight: 500
url: /tr/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

İmleci bir yer imine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |

### Geri dönüş değeri

`doğru` yer imi bulunursa;`YANLIŞ` aksi takdirde.

### Notlar

İmleci, belirtilen adındaki yer iminin başlangıcından hemen sonraki bir konuma taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa,`YANLIŞ` is döndürüldü ve imleç hareket etmiyor.

Yeni metin eklemek, yer imindeki mevcut metnin yerini almaz.

Belgedeki bazı yer imlerinin form alanlarına atandığını unutmayın. Böyle bir yer imine gitmek ve oraya metin eklemek, metni form alan koduna ekler. Bu, form alanını geçersiz kılmasa da, insert metni, alan kodunun bir parçası haline geldiğinden görünmeyecektir.

### Örnekler

Belge oluşturucunun imlecinin belgedeki farklı düğümlere nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer imi, bir yer imi başlangıç düğümünün çevrelediği düğümlerden oluşan bir varlık oluşturun,
 // ve bir yer imi bitiş düğümü.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Belge oluşturucunun imleci her zaman en son eklediğimiz düğümün önündedir.
// Oluşturucunun imleci belgenin sonundaysa, geçerli düğümü boş olacaktır.
// Önceki düğüm, en son eklediğimiz yer işareti bitiş düğümüdür.
// Oluşturucuyla yeni düğümler eklemek onları son düğüme ekleyecektir.
Assert.Null(builder.CurrentNode);

// Oluşturucu ile belgenin farklı bir bölümünü düzenlemek istiyorsak,
// imlecini düzenlemek istediğimiz düğüme getirmemiz gerekecek.
builder.MoveToBookmark("MyBookmark");

// Bunu bir yer imine taşımak, onu yer işareti başlangıç ve bitiş düğümleri içindeki ilk düğüme, yani ekteki çalıştırmaya taşıyacaktır.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// İmleci bunun gibi tek bir düğüme de taşıyabiliriz.
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

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

İmleci daha büyük bir hassasiyetle yer imine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |
| isStart | Boolean | Ne zaman`doğru` , imleci yer iminin başına taşır. Ne zaman`YANLIŞ`, imleci yer iminin sonuna taşır. |
| isAfter | Boolean | Ne zaman`doğru` , imleci Bookmark başlangıç veya bitiş konumundan sonraya taşır. Ne zaman`YANLIŞ`, imleci Bookmark başlangıç veya bitiş konumundan önceye taşır. |

### Geri dönüş değeri

`doğru` yer imi bulunursa;`YANLIŞ` aksi takdirde.

### Notlar

İmleci yer imi başlangıcından veya bitişinden önce veya sonra bir konuma taşır.

İstenilen konum satır içi düzeyde değilse bir sonraki paragrafa geçer.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa,`YANLIŞ` is döndürüldü ve imleç hareket etmiyor.

### Örnekler

Belge oluşturucunun düğüm ekleme noktası imlecinin bir yer imine nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer imi, bir BookmarkStart düğümünden ve bir BookmarkEnd düğümünden oluşur.
// yer imi adının daha sonra bir yerde eşleştirilmesi ve bu düğümlerin içerdiği içerikler.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Belge oluşturucunun imlecini yer imine taşımanın 4 yolu vardır.
// BookmarkStart ve BookmarkEnd düğümleri arasındaysak imleç yer iminin içinde olacaktır.
// Bu, oluşturucu tarafından eklenen herhangi bir metnin yer iminin bir parçası olacağı anlamına gelir.
// 1 - Yer iminin dışında, BookmarkStart düğümünün önünde:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Yer iminin içinde, BookmarkStart düğümünden hemen sonra:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - Yer iminin içinde, BookmarkEnd düğümünün hemen önünde:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Yer iminin dışında, BookmarkEnd düğümünden sonra:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


