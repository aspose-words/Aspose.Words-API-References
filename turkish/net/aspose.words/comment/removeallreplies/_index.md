---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: .NET için Aspose.Words
description: RemoveAllReplies yöntemiyle yorumunuza gelen tüm yanıtları zahmetsizce temizleyin, böylece karmaşadan uzak bir tartışma ortamı ve gelişmiş bir kullanıcı deneyimi sağlayın.
type: docs
weight: 170
url: /tr/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Bu yoruma gelen tüm yanıtları kaldırır.

```csharp
public void RemoveAllReplies()
```

## Notlar

Cevapların tüm bileşen düğümleri belgeden silinecektir.

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
