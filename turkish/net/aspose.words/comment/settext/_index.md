---
title: Comment.SetText
second_title: Aspose.Words for .NET API Referansı
description: Comment yöntem. Bu yorum metnini kolayca ayarlamaya olanak sağlayan bir kolaylık yöntemidir.
type: docs
weight: 150
url: /tr/net/aspose.words/comment/settext/
---
## Comment.SetText method

Bu, yorum metnini kolayca ayarlamaya olanak sağlayan bir kolaylık yöntemidir.

```csharp
public void SetText(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Yorumun yeni metni. |

### Notlar

Bu yöntem, bir dizeden bir yorumun metnini hızlı bir şekilde ayarlamayı sağlar. Dize, paragraf sonları içerebilir, bu, yorumda buna göre metin paragrafları oluşturur. Yoruma, örneğin bookmarks veya tablolar gibi daha karmaşık öğeler eklemek veya zengin biçimlendirme uygulamak istiyorsanız, uygun düğüm sınıflarını kullanmanız gerekir. yorum metnini oluşturmak için.

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


