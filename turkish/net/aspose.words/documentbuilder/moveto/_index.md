---
title: DocumentBuilder.MoveTo
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci satır içi düğüme veya paragrafın sonuna taşır.
type: docs
weight: 490
url: /tr/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

İmleci satır içi düğüme veya paragrafın sonuna taşır.

```csharp
public void MoveTo(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Düğüm bir paragraf veya paragrafın doğrudan alt öğesi olmalıdır. |

### Notlar

Ne zamandüğüm satır içi düzeyde bir düğümdür, imleç bu node 'ye taşınır ve bu düğümden önce daha fazla içerik eklenir.

Ne zamandüğüm bir[`Paragraph`](../../paragraph/), imleç paragraf 'nin sonuna taşınır ve paragraf sonunun hemen öncesine daha fazla içerik eklenir.

Ne zamandüğüm blok düzeyinde bir düğümdür ancak[`Paragraph`](../../paragraph/), imleç ilk paragrafın sonuna, blok düzeyindeki düğüm 'ye taşınır ve paragraf sonunun hemen öncesine daha fazla içerik eklenir.

### Örnekler

DocumentBuilder'ın imleç konumunun belirli bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucunun belgenin bir parçası olarak görev yapan bir imleci vardır
// belge oluşturma yöntemlerini kullandığımızda oluşturucunun yeni düğümler eklediği yer.
// Bu imleç Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun az önce eklediği herhangi bir düğümden hemen sonra biter.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" metodu ile imleci farklı bir düğüme taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// İmleç artık onu taşıdığımız düğümün önünde.
// İkinci bir çalıştırmanın eklenmesi onu ilk çalıştırmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Metni daha önce olduğu gibi sonuna eklemeye devam etmek için imleci belgenin sonuna taşıyın.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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


