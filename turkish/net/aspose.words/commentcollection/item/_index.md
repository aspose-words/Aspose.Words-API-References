---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: CommentCollection Item özelliğiyle belirli yorumlara zahmetsizce erişin. Kolaylaştırılmış içerik yönetimi için yorumları dizine göre alın.
type: docs
weight: 10
url: /tr/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Birini alır[`Comment`](../../comment/) verilen indekste.

```csharp
public Comment this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

## Örnekler

Yorum yanıtlarının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Aşağıda bir yorumdan yanıtları kaldırmanın iki yolu bulunmaktadır.
// 1 - Bir yorumdan gelen yanıtları tek tek kaldırmak için "RemoveReply" yöntemini kullanın:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Bir yorumdan tüm yanıtları tek seferde kaldırmak için "RemoveAllReplies" yöntemini kullanın:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Ayrıca bakınız

* class [Comment](../../comment/)
* class [CommentCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
