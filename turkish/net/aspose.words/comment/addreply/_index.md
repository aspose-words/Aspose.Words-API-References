---
title: Comment.AddReply
second_title: Aspose.Words for .NET API Referansı
description: Comment yöntem. Bu yoruma bir yanıt ekler.
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
| author | String | Yanıt için yazar adı. |
| initial | String | Yazar cevap için baş harfleri. |
| dateTime | DateTime | Yanıtın tarihi ve saati. |
| text | String | Cevap metni. |

### Geri dönüş değeri

oluşturulan[`Comment`](../) cevap için düğüm.

### Notlar

Mevcut MS Office sınırlamaları nedeniyle, belgede yalnızca 1 yanıt düzeyine izin verilir. Bir tür istisnasıInvalidOperationException bu yöntem mevcut Yanıt yorumunda çağrılırsa yükseltilecektir.

### Örnekler

Bir belgeye nasıl yorum ekleneceğini ve ardından nasıl yanıtlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Yorumu belgenin gövdesindeki bir düğüme yerleştirin.
// Bu yorum paragrafının bulunduğu yerde görünecek,
// sayfanın sağ kenar boşluğunun dışında ve onu paragrafına bağlayan noktalı bir çizgi ile.
builder.CurrentParagraph.AppendChild(comment);

// Üst yorumunun altında görünecek bir yanıt ekleyin.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Yorumlar ve yanıtların her ikisi de Yorum düğümleridir.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Diğer yorumlara cevap vermeyen yorumlar "üst düzey"dir. Ata yorumları yoktur.
Assert.Null(comment.Ancestor);

// Yanıtların üst düzey bir yorumu var.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ayrıca bakınız

* class [Comment](../)
* ad alanı [Aspose.Words](../../comment/)
* toplantı [Aspose.Words](../../../)


