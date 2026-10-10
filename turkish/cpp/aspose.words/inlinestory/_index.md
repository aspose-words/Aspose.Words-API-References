---
title: "Aspose::Words::InlineStory sınıfı"
linktitle: "InlineStory"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::InlineStory sınıfı. Paragraflar ve tablolar içerebilen satır içi düzey düğümler için temel sınıftır. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 37000
url: /tr/cpp/aspose.words/inlinestory/
---
## InlineStory class


Paragraflar ve tablolar içerebilen satır içi düzey düğümler için temel sınıftır. Daha fazla bilgi edinmek için [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class InlineStory : public Aspose::Words::CompositeNode,
                    public Aspose::Words::IInline,
                    public Aspose::Words::IStory
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd metodunu çağırır. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart metodunu çağırır. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [EnsureMinimum](./ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Hikayedeki ilk paragrafı alır. |
| [get_Font](./get_font/)() | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastParagraph](./get_lastparagraph/)() override | Hikayedeki son paragrafı alır. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_Paragraphs](./get_paragraphs/)() override | Hikayenin doğrudan çocukları olan paragraf koleksiyonunu alır. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](./get_parentparagraph/)() | Bu düğümün üst [Paragraph](../paragraph/) öğesini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| virtual [get_StoryType](./get_storytype/)() | Story'nin türünü döndürür. |
| [get_Tables](./get_tables/)() override | Hikayenin doğrudan çocukları olan tablo koleksiyonunu alır. |
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
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../node/) öğesini seçer. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[InlineStory](./) is a container for block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

[InlineStory](./) sınıfından türetilen sınıflar, kendi metinlerini (paragraflar ve tablolar) içerebilen satır içi düzey düğümlerdir. Örneğin, bir [Comment](../comment/) düğümü bir yorumun metnini ve bir [Footnote](../../aspose.words.notes/footnote/) bir dipnotun metnini içerir.

## Örnekler



Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metin ekleyin ve bir dipnot ile referans verin. Bu dipnot, küçük bir üst simge referansı yerleştirecek
// referans verdiği metnin ardından bir işaret koyacak ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturacaktır.
// Bu giriş, dipnotun referans işaretini ve referans metnini içerecektir,
// bunu belge oluşturucunun "InsertFootnote" metoduna geçireceğiz.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Bu özellik "true" olarak ayarlanırsa, dipnotumuzun referans işareti
// bölümdeki tüm dipnotlar arasında indeksine eşit olacaktır.
// Bu ilk dipnottur, bu yüzden referans işareti "1" olacaktır.
ASSERT_TRUE(footnote->get_IsAuto());

// Belge oluşturucuyu dipnotun içine taşıyarak referans metnini düzenleyebiliriz.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti ayarlayabiliriz.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// "IsAuto" bayrağı true olarak ayarlı bir yer imi hâlâ gerçek indeksini gösterecektir
// önceki yer imleri özel referans işaretleri gösterse bile, bu yer iminin referans işareti "3" olacaktır.
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
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

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
