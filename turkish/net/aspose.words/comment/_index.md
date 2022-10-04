---
title: Comment
second_title: Aspose.Words for .NET API Referansı
description: Yorum metni için bir kapsayıcıyı temsil eder.
type: docs
weight: 220
url: /tr/net/aspose.words/comment/
---
## Comment class

Yorum metni için bir kapsayıcıyı temsil eder.

```csharp
public sealed class Comment : InlineStory
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Yeni bir örneğini başlatır **Yorum** sınıf. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Yeni bir örneğini başlatır **Yorum** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Üst Yorum nesnesini döndürür. Üst düzey yorumlar için null döndürür. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Bir yorum için yazar adını döndürür veya ayarlar. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Yorumun yapıldığı tarih ve saati alır. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Yorumun tamamlandı olarak işaretlendiğini belirten bayrağı alır veya ayarlar. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Öyküdeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [Id](../../aspose.words/comment/id/) { get; } | Yorum tanımlayıcısını alır. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Belirli bir yorumla ilişkili kullanıcının baş harflerini döndürür veya ayarlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Öyküdeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | İade **DüğümTürü.Yorum** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Öykünün doğrudan alt öğeleri olan bir paragraf koleksiyonu alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Bir koleksiyon döndürür[`Comment`](./comment/) belirtilen yorumun hemen alt öğeleri olan nesneler. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | İade **StoryType.Yorumlar** . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Öykünün doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Bu yoruma bir yanıt ekler. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son alt öğe bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Bu yoruma verilen tüm yanıtları kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Bu yoruma verilen belirtilen yanıtı kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [SetText](../../aspose.words/comment/settext/)(string) | Bu, yorum metnini kolayca ayarlamaya olanak sağlayan bir kolaylık yöntemidir. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Yorum, metnin bir bölgesine veya metindeki bir konuma sabitlenmiş bir açıklamadır. Bir yorum, rastgele miktarda blok düzeyinde içerik içerebilir.

Eğer bir[`Comment`](./comment/) nesne kendi kendine oluşur, yorum nesnenin konumuna sabitlenir.[`Comment`](./comment/) nesne.

Metnin bir bölgesine bir yorum tutturmak için üç nesne gereklidir:[`Comment`](./comment/) , [`CommentRangeStart`](../commentrangestart/) ve[`CommentRangeEnd`](../commentrangeend/) Her üç nesnenin de aynı öğesini paylaşması gerekir[`Id`](./id/) değer.

[`Comment`](./comment/) satır içi düzey bir düğümdür ve yalnızca alt öğesi olabilir[`Paragraph`](../paragraph/).

[`Comment`](./comment/) içerebilir[`Paragraph`](../paragraph/) ve[`Table`](../../aspose.words.tables/table/) alt düğümler.

### Örnekler

Bir paragrafa nasıl yorum ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// Microsoft Word'de, düzenlemek veya yanıtlamak için belge gövdesindeki bu yorumu sağ tıklatabiliriz. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

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

* class [InlineStory](../inlinestory/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
