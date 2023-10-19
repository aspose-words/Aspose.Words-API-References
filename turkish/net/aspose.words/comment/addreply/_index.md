---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words for .NET
description: Comment AddReply yöntem. Bu yoruma bir yanıt ekler C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Bu yoruma bir yanıt ekler.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Yanıtın yazarının adı. |
| initial | String | Yazar yanıtın baş harflerini kullanır. |
| dateTime | DateTime | Yanıtın tarihi ve saati. |
| text | String | Cevap metni. |

### Geri dönüş değeri

Yaratılan[`Comment`](../) yanıt için düğüm.

## Notlar

Mevcut MS Office sınırlamaları nedeniyle belgede yalnızca 1 düzeyde yanıta izin verilir. Bir tür istisnaInvalidOperationException bu yöntem mevcut Yanıt yorumunda olarak çağrılırsa tetiklenecektir.

## Örnekler

Bir belgeye nasıl yorum ekleneceğini ve ardından ona nasıl yanıt verileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Yorumu belgenin gövdesindeki bir düğüme yerleştirin.
// Bu yorum paragrafın bulunduğu yerde görünecek,
// sayfanın sağ kenar boşluğunun dışında ve onu paragrafına bağlayan noktalı bir çizgiyle.
builder.CurrentParagraph.AppendChild(comment);

// Ana yorumun altında görünecek bir yanıt ekleyin.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Yorumlar ve yanıtların her ikisi de Yorum düğümleridir.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Diğer yorumlara cevap vermeyen yorumlar "üst seviye"dir. Ata yorumlarına sahip değiller.
Assert.Null(comment.Ancestor);

// Yanıtların üst düzey bir yorumu var.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ayrıca bakınız

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
