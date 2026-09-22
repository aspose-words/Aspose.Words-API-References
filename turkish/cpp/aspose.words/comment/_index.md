---
title: "Aspose::Words::Comment sınıfı"
linktitle: "Yorum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment sınıfı. Bir yorumun metni için bir kapsayıcıyı temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/comment/
---
## Comment class


Bir yorumun metni için bir kapsayıcıyı temsil eder. Daha fazla bilgi edinmek için [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) dokümantasyon makalesini ziyaret edin.

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Yorumun sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Yorumun başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Bu yoruma bir yanıt ekler. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | [Comment](./) sınıfının yeni bir örneğini başlatır. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | [Comment](./) sınıfının yeni bir örneğini başlatır. |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [get_Ancestor](./get_ancestor/)() | Üst [Comment](./) nesnesini döndürür. Üst düzey yorumlar için **null** döndürür. |
| [get_Author](./get_author/)() const | Bir yorum için yazar adını döndürür veya ayarlar. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_DateTime](./get_datetime/)() const | Yorumun yapıldığı tarih ve saati alır. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Yorumun yapıldığı UTC tarih ve saatini alır. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Done](./get_done/)() const | Yorumun tamamlandı olarak işaretlenip işaretlenmediğini gösteren bayrağı alır veya ayarlar. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Hikayedeki ilk paragrafı alır. |
| [get_Font](../inlinestory/get_font/)() | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_Id](./get_id/)() const | Yorum tanımlayıcısını alır veya ayarlar. |
| [get_Initial](./get_initial/)() const | Belirli bir yorumla ilişkili kullanıcının baş harflerini döndürür veya ayarlar. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Hikayedeki son paragrafı alır. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [Comment](../nodetype/) döndürür. |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Hikayenin doğrudan çocukları olan paragraf koleksiyonunu alır. |
| [get_ParentId](./get_parentid/)() const | Üst yorum kimliğini alır. **%-1** değeri, yorumun üst yorumunun olmadığını gösterir. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../paragraph/) öğesini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_Replies](./get_replies/)() | Belirtilen yorumun doğrudan alt öğeleri olan [Comment](./) nesnelerinin bir koleksiyonunu döndürür. |
| [get_StoryType](./get_storytype/)() override | [Comments](../storytype/) döndürür. |
| [get_Tables](../inlinestory/get_tables/)() override | Hikayenin doğrudan çocukları olan tablo koleksiyonunu alır. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveAllReplies](./removeallreplies/)() | Bu yoruma yapılan tüm yanıtları kaldırır. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Bu yorum için belirtilen yanıtı kaldırır. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../node/) öğesini seçer. |
| [set_Author](./set_author/)(const System::String\&) | [Aspose::Words::Comment::get_Author](./get_author/) için ayarlayıcı. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_DateTime](./set_datetime/)(System::DateTime) | Yorumun yapıldığı tarih ve saati alır. |
| [set_Done](./set_done/)(bool) | [Aspose::Words::Comment::get_Done](./get_done/) için ayarlayıcı. |
| [set_Id](./set_id/)(int32_t) | [Aspose::Words::Comment::get_Id](./get_id/) için ayarlayıcı. |
| [set_Initial](./set_initial/)(const System::String\&) | [Aspose::Words::Comment::get_Initial](./get_initial/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Üst yorum kimliğini ayarlar. **%-1** değeri, yorumun üst yorumunun olmadığını gösterir. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Bu, yorum metnini kolayca ayarlamayı sağlayan bir kolaylık yöntemidir. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Yorum, metin bölgesine ya da metin içindeki bir konuma bağlanan bir açıklamadır. Yorum, blok düzeyinde isteğe bağlı miktarda içerik içerebilir.

Bir [Comment](./) nesnesi tek başına bulunursa, yorum [Comment](./) nesnesinin konumuna bağlanır.

Bir yorumu metin bölgesine bağlamak için üç nesne gerekir: [Comment](./), [CommentRangeStart](../commentrangestart/) ve [CommentRangeEnd](../commentrangeend/). Bu üç nesnenin aynı [Id](./get_id/) değerini paylaşması gerekir.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Örnekler



Bir belgeye yorum eklemeyi ve ardından ona yanıt vermeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Yorumu belgenin gövdesindeki bir düğüme yerleştirin.
// Bu yorum, paragrafının konumunda görünecek,
// sayfanın sağ kenar boşluğunun dışında ve paragrafına noktalı bir çizgiyle bağlanarak.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Üst yorumun altında görünecek bir yanıt ekleyin.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Yorumlar ve yanıtlar her ikisi de Comment düğümüdür.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Diğer yorumlara yanıt vermeyen yorumlar "üst düzey"dir. Bunların üst yorumları yoktur.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Yanıtların bir üst düzey yorum üst öğesi vardır.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Bir paragrafa yorum eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// Microsoft Word'te, belge gövdesindeki bu yoruma sağ tıklayarak düzenleyebilir veya yanıtlayabiliriz.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Ayrıca Bakınız

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
