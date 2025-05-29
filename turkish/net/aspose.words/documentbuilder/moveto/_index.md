---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: .NET için Aspose.Words
description: Satır içi düğümlerde kolayca gezinmek ve sorunsuz belge düzenleme için imlecinizi paragraf sonlarına etkili bir şekilde yerleştirmek amacıyla DocumentBuilder MoveTo yöntemini keşfedin.
type: docs
weight: 520
url: /tr/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

İmleci satır içi bir düğüme veya bir paragrafın sonuna taşır.

```csharp
public void MoveTo(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Düğüm bir paragraf veya doğrudan bir paragrafın alt öğesi olmalıdır. |

## Notlar

Ne zamandüğüm satır içi düzeyde bir düğümdür, imleç bu node 'ye taşınır ve bu düğümden önce daha fazla içerik eklenir.

Ne zamandüğüm bir[`Paragraph`](../../paragraph/)imleç paragrafın sonuna taşınır ve paragraf sonundan hemen öncesine daha fazla içerik eklenir.

Ne zamandüğüm blok düzeyinde bir düğümdür ancak bir[`Paragraph`](../../paragraph/), imleç blok düzeyindeki node ilk paragrafın sonuna taşınır ve paragraf sonundan hemen öncesine daha fazla içerik eklenir.

## Örnekler

Bir DocumentBuilder'ın imleç konumunun belirtilen bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucunun, belgenin bir parçası olarak işlev gören bir imleci vardır
// Oluşturucunun belge oluşturma yöntemlerini kullandığımızda yeni düğümler eklediği yer.
// Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun eklediği herhangi bir düğümün hemen ardından sonlanır.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" metodu ile imleci farklı bir düğüme taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// İmleç artık onu taşıdığımız düğümün önünde.
// İkinci bir çalışma eklemek, onu ilk çalışmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Metni daha önce olduğu gibi belgenin sonuna eklemeye devam etmek için imleci belgenin sonuna getirin.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
