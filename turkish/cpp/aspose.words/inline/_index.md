---
title: "Aspose::Words::Inline sınıf"
linktitle: "Satır içi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Inline sınıf. Karakter biçimlendirmesiyle ilişkilendirilebilen satır içi düzeyindeki düğümler için temel sınıf, ancak kendi alt düğümlerine sahip olamaz. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 36000
url: /tr/cpp/aspose.words/inline/
---
## Inline class


Kendi alt düğümlerine sahip olamayan, ancak karakter biçimlendirmesiyle ilişkilendirilebilen satır içi düzey düğümler için temel sınıftır. Daha fazla bilgi edinmek için [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Font](./get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](./get_parentparagraph/)() | Bu düğümün üst [Paragraph](../paragraph/) öğesini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../node/remove/)() | Kendisini üst düğümden kaldırır. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[Inline](./) üzerinden türetilen bir sınıf, [Paragraph](../paragraph/) öğesinin çocuğu olabilir.

## Örnekler



Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Belgeyi, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği açıkken düzenlediğimizde,
// Microsoft Word'de etkinleştirildiğinde, yaptığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon izlemeye şu şekilde başlayabiliriz
// "StartTrackRevisions" yöntemini belge üzerinde çağırarak ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durdurabilirsiniz.
// Revizyonları kabul ederek belgeye dahil edebiliriz
// veya reddederek önerilen değişikliği etkili bir şekilde iptal edebiliriz.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Bir revizyonun üst düğümü, revizyonun ilgili olduğu Run'dur. Run, bir Inline düğümdür.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Aşağıda bir Inline düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
// 1 -  Bir "insert" revizyonu:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde ortaya çıkar.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Bir "format" revizyonu:
// Bu revizyon, değişiklikleri izlerken metnin biçimlendirmesini değiştirdiğimizde ortaya çıkar.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Bir "move from" revizyonu:
// Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir yere sürüklediğimizde
// değişiklikleri izlerken iki revizyon ortaya çıkar.
// "move from" revizyonu, metni taşımadan önceki orijinal kopyasıdır.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Bir "move to" revizyonu:
// "move to" revizyonu, belge içinde yeni konumunda taşıdığımız metindir.
// "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
// ve "move to" revizyonundaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Bir "delete" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde ortaya çıkar. Böyle bir metni sildiğimizde,
// metin, revizyonu kabul edene kadar belge içinde bir revizyon olarak kalır,
// bu, metni kalıcı olarak siler; ya da revizyonu reddeder, bu da sildiğimiz metni olduğu yerde tutar.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Ayrıca Bakınız

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
