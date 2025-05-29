---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: .NET için Aspose.Words
description: Yorum EkleCevap yöntemiyle tartışmalarınızı geliştirin; yorumlara kolayca yanıt ekleyin ve platformunuzdaki etkileşimi artırın!
type: docs
weight: 160
url: /tr/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Bu yoruma bir yanıt ekler.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Cevap için yazar adı. |
| initial | String | Yazar cevap için paraf atıyor. |
| dateTime | DateTime | Cevap için tarih ve saat. |
| text | String | Cevap metni. |

### Geri dönüş değeri

Yaratılan[`Comment`](../) cevap için düğüm.

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidOperationException | Bu metot mevcut Cevap yorumunda çağrılırsa fırlatılır. |

## Notlar

Mevcut MS Office sınırlamaları nedeniyle belgede yalnızca 1 düzeyde yanıta izin verilmektedir.

## Örnekler

Bir belgeye nasıl yorum ekleneceğini ve ardından buna nasıl yanıt verileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Yorumu belgenin gövdesindeki bir düğüme yerleştirin.
// Bu yorum, paragrafının bulunduğu yerde gösterilecektir.
// Sayfanın sağ kenar boşluğunun dışında ve paragrafına noktalı bir çizgiyle bağlanıyor.
builder.CurrentParagraph.AppendChild(comment);

// Üst yorumunun altında görünecek bir yanıt ekleyin.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Yorumlar ve yanıtlar her ikisi de Yorum düğümleridir.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Diğer yorumlara yanıt vermeyen yorumlar "en üst düzey"dir. Bunların ata yorumları yoktur.
Assert.Null(comment.Ancestor);

// Cevapların üst düzey bir yorumu vardır.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ayrıca bakınız

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
