---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: CommentCollection Item mülk. Bir öğeyi alırComment verilen dizinde C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Bir öğeyi alır[`Comment`](../../comment/) verilen dizinde.

```csharp
public Comment this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyona bir dizin. |

## Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

## Örnekler

Yorum yanıtlarının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Aşağıda bir yorumdan yanıtları kaldırmanın iki yolu verilmiştir.
// 1 - Bir yorumdaki yanıtları tek tek kaldırmak için "RemoveReply" yöntemini kullanın:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - Bir yorumdaki tüm yanıtları tek seferde kaldırmak için "RemoveAllReplies" yöntemini kullanın:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Ayrıca bakınız

* class [Comment](../../comment/)
* class [CommentCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
