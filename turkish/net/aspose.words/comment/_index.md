---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: .NET için Aspose.Words
description: Belgelerdeki yorum metinlerini yönetmek için temel aracınız olan Aspose.Words.Comment sınıfını keşfedin. Sorunsuz entegrasyonla iş akışınızı geliştirin!
type: docs
weight: 420
url: /tr/net/aspose.words/comment/
---
## Comment class

Bir yorumun metni için bir kapsayıcıyı temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yorumlarla Çalışma](https://docs.aspose.com/words/net/working-with-comments/) belgeleme makalesi.

```csharp
public sealed class Comment : InlineStory
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Yeni bir örneğini başlatır`Comment` sınıf. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Yeni bir örneğini başlatır`Comment` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Üst öğeyi döndürür`Comment`nesne. Geri döner`hükümsüz` en üst düzey yorumlar için. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Bir yorumun yazar adını döndürür veya ayarlar. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Yorumun yapıldığı tarih ve saati alır. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Yorumun yapıldığı UTC tarih ve saatini alır. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Yorumun yapıldığına işaret edildiğini belirten bayrağı alır veya ayarlar. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Hikayedeki ilk paragrafı alır. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Yorum tanımlayıcısını alır veya ayarlar. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Belirli bir yorumla ilişkili kullanıcının baş harflerini döndürür veya ayarlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hikayedeki son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | Geri DöndürürComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Üst yorum kimliğini alır veya ayarlar. Bir değer`-1` yorumun ebeveyni olmadığı anlamına gelir. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Bir koleksiyon döndürür`Comment` belirtilen yorumun doğrudan çocukları olan nesneler. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | Geri DöndürürComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Hikayenin doğrudan alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Yorumun sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Yorumun başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Bu yoruma bir yanıt ekler. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Bu yoruma gelen tüm yanıtları kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Bu yoruma verilen belirtilen yanıtı kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../node/) XPath ifadesiyle eşleşen. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Bu, yorumun metnini kolayca ayarlamanıza olanak tanıyan kullanışlı bir yöntemdir. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Yorum, metnin bir bölgesine veya metindeki bir konuma sabitlenmiş bir açıklamadır. Yorum, blok düzeyinde keyfi miktarda içerik barındırabilir.

Eğer bir`Comment` nesne kendi başına meydana geldiğinde, yorum, nesnenin konumuna sabitlenir.`Comment` nesne.

Bir yorumu metnin bir bölgesine bağlamak için üç nesne gereklidir:`Comment` , [`CommentRangeStart`](../commentrangestart/) Ve[`CommentRangeEnd`](../commentrangeend/) . Her üç nesnenin de aynı değerini paylaşması gerekir[`Id`](./id/) değer.

`Comment` satır içi düzeyde bir düğümdür ve yalnızca bir alt düğüm olabilir[`Paragraph`](../paragraph/).

`Comment` içerebilir[`Paragraph`](../paragraph/) Ve[`Table`](../../aspose.words.tables/table/) çocuk düğümleri.

## Örnekler

Bir paragrafa yorum eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // Microsoft Word'de, bu yorumu belge gövdesinde sağ tıklayarak düzenleyebilir veya yanıtlayabiliriz.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

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

* class [InlineStory](../inlinestory/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
