---
title: Comment.SetText
second_title: Aspose.Words for .NET API Referansı
description: Comment yöntem. Bu yorum metnini kolayca ayarlamanıza olanak tanıyan kullanışlı bir yöntemdir.
type: docs
weight: 180
url: /tr/net/aspose.words/comment/settext/
---
## Comment.SetText method

Bu, yorum metnini kolayca ayarlamanıza olanak tanıyan kullanışlı bir yöntemdir.

```csharp
public void SetText(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Yorumun yeni metni. |

### Notlar

Bu yöntem, bir dizeden bir yorumun metninin hızlı bir şekilde ayarlanmasına olanak tanır. Dize paragraf sonlarını içerebilir, bu da yorumda buna göre paragraflar oluşturacaktır. Yoruma daha karmaşık öğeler (örneğin, yer imleri veya tablolar) eklemek veya zengin biçimlendirme uygulamak istiyorsanız, uygun düğüm sınıflarını kullanmanız gerekir. yorum metnini oluşturmak için.

### Örnekler

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
* ad alanı [Aspose.Words](../../comment/)
* toplantı [Aspose.Words](../../../)


