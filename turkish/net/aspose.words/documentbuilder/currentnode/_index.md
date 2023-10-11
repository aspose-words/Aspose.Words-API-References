---
title: DocumentBuilder.CurrentNode
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. Bu DocumentBuilderda seçili olan düğümü alır.
type: docs
weight: 40
url: /tr/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Bu DocumentBuilder'da seçili olan düğümü alır.

```csharp
public Node CurrentNode { get; }
```

### Notlar

`CurrentNode` bir imleçtir[`DocumentBuilder`](../) ve bir noktaya işaret ediyor[`Node`](../../node/) bu doğrudan bir alt öğedir[`Paragraph`](../../paragraph/) . kullanarak gerçekleştirdiğiniz tüm ekleme işlemleri[`DocumentBuilder`](../) önce eklenecek`CurrentNode`.

Geçerli paragraf boş olduğunda veya imleç bir paragrafın veya yapılandırılmış belge etiketinin sonundan hemen önce konumlandırıldığında,`CurrentNode` İadeler`hükümsüz`.

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


