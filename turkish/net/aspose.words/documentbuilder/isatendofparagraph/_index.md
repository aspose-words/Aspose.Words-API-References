---
title: DocumentBuilder.IsAtEndOfParagraph
linktitle: IsAtEndOfParagraph
articleTitle: IsAtEndOfParagraph
second_title: .NET için Aspose.Words
description: Belge düzenlemede sorunsuz bir şekilde ilerlemek için imlecin bir paragrafın sonunda konumlanıp konumlanmadığını etkin bir şekilde kontrol eden DocumentBuilder'ın IsAtEndOfParagraph özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words/documentbuilder/isatendofparagraph/
---
## DocumentBuilder.IsAtEndOfParagraph property

Geri Döndürür`doğru` imleç geçerli paragrafın sonunda ise.

```csharp
public bool IsAtEndOfParagraph { get; }
```

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
