---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: .NET için Aspose.Words
description: Yorum eklemeyi kolaylaştıran, iş akışınızı geliştiren ve üretkenliğinizi zahmetsizce artıran, kullanıcı dostu bir araç olan SetText yöntemini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words/comment/settext/
---
## Comment.SetText method

Bu, yorumun metnini kolayca ayarlamanıza olanak tanıyan kullanışlı bir yöntemdir.

```csharp
public void SetText(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Yorumun yeni metni. |

## Notlar

Bu yöntem, bir yorumun metnini bir dizgeden hızlı bir şekilde ayarlamanıza olanak tanır. Dizge, paragraf sonları içerebilir, bu, yorumda buna göre metin paragrafları oluşturur. Yoruma daha karmaşık öğeler eklemek istiyorsanız, örneğin bookmarks veya tablolar veya zengin biçimlendirme uygulamak istiyorsanız, yorum metnini oluşturmak için uygun düğüm sınıflarını kullanmanız gerekir.

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
