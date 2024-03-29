---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words for .NET
description: Comment RemoveAllReplies yöntem. Bu yoruma verilen tüm yanıtları kaldırır C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Bu yoruma verilen tüm yanıtları kaldırır.

```csharp
public void RemoveAllReplies()
```

## Notlar

Yanıtların tüm bileşen düğümleri belgeden silinecektir.

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

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
