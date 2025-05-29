---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: .NET için Aspose.Words
description: İstenmeyen yanıtları Comment RemoveReply yöntemiyle zahmetsizce kaldırın, tartışmalarınızın net ve alakalı kalmasını sağlayın. Yorum yönetiminizi bugün geliştirin!
type: docs
weight: 180
url: /tr/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Bu yoruma verilen belirtilen yanıtı kaldırır.

```csharp
public void RemoveReply(Comment reply)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| reply | Comment | Silinen yanıtın yorum düğümü. |

## Notlar

Yanıtın tüm bileşen düğümleri belgeden silinecektir.

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

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
