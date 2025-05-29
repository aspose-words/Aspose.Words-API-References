---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToBookmark yöntemiyle belgelerinizde zahmetsizce gezinin, gelişmiş düzenleme için imleci anında herhangi bir yer işaretine konumlandırın.
type: docs
weight: 530
url: /tr/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

İmleci bir yer imine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |

### Geri dönüş değeri

`doğru` yer imi bulunduysa;`YANLIŞ` aksi takdirde.

## Notlar

İmleci, belirtilen ada sahip yer iminin başlangıcından hemen sonraki bir konuma taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamadıysa,`YANLIŞ` is döndürüldü ve imleç hareket ettirilmedi.

Yeni metin eklemek, yer iminin mevcut metnini değiştirmez.

Belgedeki bazı yer imlerinin form alanlarına atandığını unutmayın. Böyle bir yer imine gidip oraya metin eklemek, metni form alan koduna ekler. Bu, form alanını geçersiz kılmasa da, inserted metni alan kodunun bir parçası haline geldiği için görünmez.

## Örnekler

Bir belge oluşturucunun imlecinin bir belgedeki farklı düğümlere nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yer imi başlangıç düğümü tarafından çevrelenen düğümlerden oluşan bir varlık olan geçerli bir yer imi oluşturun,
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
// Eğer oluşturucunun imleci belgenin sonunda ise, geçerli düğümü boş olacaktır.
// Önceki düğüm, en son eklediğimiz yer imi son düğümüdür.
// Builder ile yeni düğümler eklendiğinde, bunlar son düğüme eklenecektir.
Assert.Null(builder.CurrentNode);

// Belgenin farklı bir bölümünü oluşturucuyla düzenlemek istersek,
// Düzenlemek istediğimiz düğüme imleci getirmemiz gerekecek.
builder.MoveToBookmark("MyBookmark");

// Bunu bir yer imine taşımak, onu yer imi başlangıç ve bitiş düğümleri içindeki ilk düğüme, yani kapalı çalışmaya taşıyacaktır.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// İmleci bu şekilde tek bir düğüme de taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Bir belgenin başına/sonuna gitmek için belirli yöntemleri kullanabiliriz.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

İmleci daha büyük bir hassasiyetle bir yer imine taşır.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | İmlecin taşınacağı yer iminin adı. |
| isStart | Boolean | Ne zaman`doğru` , imleci yer iminin başına taşır. `YANLIŞ`, imleci yer iminin sonuna taşır. |
| isAfter | Boolean | Ne zaman`doğru` , imleci bookmark başlangıç veya bitiş konumundan sonraya taşır.`YANLIŞ`imleci bookmark başlangıç veya bitiş konumundan önceye taşır. |

### Geri dönüş değeri

`doğru` yer imi bulunduysa;`YANLIŞ` aksi takdirde.

## Notlar

İmleci yer imi başlangıcından veya bitişinden önceki veya sonraki bir konuma taşır.

İstenilen konum satır içi düzeyde değilse bir sonraki paragrafa geçer.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamadıysa,`YANLIŞ` is döndürüldü ve imleç hareket ettirilmedi.

## Örnekler

Bir belge oluşturucunun düğüm ekleme noktası imlecinin bir yer imine nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer imi, bir BookmarkStart düğümünden, bir BookmarkEnd düğümünden oluşur.
// sonrasında bir yerde eşleşen yer imi adı ve bu düğümlerin çevrelediği içerikler.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Bir belge oluşturucunun imlecini bir yer imine taşımanın 4 yolu vardır.
// Eğer BookmarkStart ve BookmarkEnd düğümleri arasındaysak, imleç yer iminin içerisinde olacaktır.
// Bu, oluşturucu tarafından eklenen herhangi bir metnin yer iminin bir parçası olacağı anlamına gelir.
// 1 - Yer işaretinin dışında, BookmarkStart düğümünün önünde:
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

// 4 - Yer işaretinin dışında, BookmarkEnd düğümünden sonra:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
