---
title: "Aspose::Words::Notes::Footnote sınıfı"
linktitle: "Footnote"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::Footnote sınıfı. Bir dipnot ya da sonnot metni için bir kapsayıcıyı temsil eder. Daha fazla bilgi edinmek için C++'daki belgeler makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.notes/footnote/
---
## Footnote class


Bir dipnot veya altnot metni için bir kapsayıcıyı temsil eder. Daha fazla bilgi için, [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/) dokümantasyon makalesini ziyaret edin.

```cpp
class Footnote : public Aspose::Words::InlineStory,
                 public Aspose::Words::Revisions::ITrackableNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Dipnotun sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Dipnotun başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [Footnote](./footnote/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Notes::FootnoteType) | [Footnote](./) sınıfının bir örneğini başlatır. |
| [get_ActualReferenceMark](./get_actualreferencemark/)() | Bu dipnot için belgede gösterilen referans işaretinin gerçek metnini alır. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstParagraph](../../aspose.words/inlinestory/get_firstparagraph/)() override | Hikayedeki ilk paragrafı alır. |
| [get_Font](../../aspose.words/inlinestory/get_font/)() | Bu nesnenin bağlantı karakterinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_FootnoteType](./get_footnotetype/)() const | Bu nesnenin dipnot mu yoksa sonnot mu olduğunu belirten bir değer döndürür. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsAuto](./get_isauto/)() const | Bu nesnenin otomatik numaralı bir dipnot mu yoksa kullanıcı tanımlı özel referans işaretli bir dipnot mu olduğunu belirten bir değeri tutar. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDeleteRevision](../../aspose.words/inlinestory/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsInsertRevision](../../aspose.words/inlinestory/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](../../aspose.words/inlinestory/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../../aspose.words/inlinestory/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastParagraph](../../aspose.words/inlinestory/get_lastparagraph/)() override | Hikayedeki son paragrafı alır. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [Footnote](../../aspose.words/nodetype/) döndürür. |
| [get_Paragraphs](../../aspose.words/inlinestory/get_paragraphs/)() override | Hikayenin doğrudan çocukları olan paragraf koleksiyonunu alır. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../../aspose.words/inlinestory/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../../aspose.words/paragraph/) öğesini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_ReferenceMark](./get_referencemark/)() const | Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer **empty string**'dir, bu da otomatik numaralı dipnotların kullanıldığı anlamına gelir. |
| [get_StoryType](./get_storytype/)() override | [Footnotes](../../aspose.words/storytype/) veya [Endnotes](../../aspose.words/storytype/) döndürür. |
| [get_Tables](../../aspose.words/inlinestory/get_tables/)() override | Hikayenin doğrudan çocukları olan tablo koleksiyonunu alır. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../../aspose.words/node/) öğesini seçer. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_IsAuto](./set_isauto/)(bool) | [Aspose::Words::Notes::Footnote::get_IsAuto](./get_isauto/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ReferenceMark](./set_referencemark/)(const System::String\&) | [Aspose::Words::Notes::Footnote::get_ReferenceMark](./get_referencemark/) için ayarlayıcı. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[Footnote](./) sınıfı, bir Word belgesinde hem dipnotları hem de sonnotları temsil etmek için kullanılır.

[Footnote](./) is an inline-level node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[Footnote](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

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

## Ayrıca Bakınız

* Class [InlineStory](../../aspose.words/inlinestory/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
