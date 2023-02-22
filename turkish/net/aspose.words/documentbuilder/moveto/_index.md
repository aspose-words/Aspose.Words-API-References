---
title: DocumentBuilder.MoveTo
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci satır içi bir düğüme veya paragrafın sonuna taşır.
type: docs
weight: 460
url: /tr/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

İmleci satır içi bir düğüme veya paragrafın sonuna taşır.

```csharp
public void MoveTo(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Düğüm, bir paragraf veya bir paragrafın doğrudan çocuğu olmalıdır. |

### Notlar

Ne zamandüğüm satır içi düzeyde bir düğümse, imleç bu düğüme taşınır ve bu düğümden önce daha fazla içerik eklenecektir.

Ne zamandüğüm bir **Paragraf**, imleç paragraf 'nin sonuna taşınır ve daha fazla içerik paragraf sonundan hemen önce eklenir.

Ne zamandüğümblok düzeyinde bir düğümdür, ancak bir Paragraf değildir, imleç blok düzeyindeki node içine ilk paragrafın sonuna taşınır ve paragraf sonundan hemen önce daha fazla içerik eklenecektir.

### Örnekler

DocumentBuilder'ın imleç konumunun belirli bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucu, belgenin parçası olarak işlev gören bir imleç içerir
// belge oluşturma yöntemlerini kullandığımızda oluşturucunun yeni düğümler eklediği yer.
// Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun yeni eklediği herhangi bir düğümden hemen sonra biter.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" yöntemi ile imleci farklı bir düğüme taşıyabiliriz.
// İmleç şimdi onu taşıdığımız düğümün önündedir.
// İkinci bir çalıştırma eklemek, onu ilk çalıştırmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Daha önce olduğu gibi sonuna metin eklemeye devam etmek için imleci belgenin sonuna taşıyın.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


