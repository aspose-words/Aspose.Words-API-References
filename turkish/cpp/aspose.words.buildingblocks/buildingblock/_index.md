---
title: "Aspose::Words::BuildingBlocks::BuildingBlock class"
linktitle: "BuildingBlock"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::BuildingBlock class. Bir sözlük belge girişi, örneğin **Building Block**, AutoText veya AutoCorrect girişi temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


Bir Yapı Bloğu, Otomatik Metin veya Otomatik Düzeltme girişi gibi bir sözlük belge girdisini temsil eder. Daha fazla bilgi için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class BuildingBlock : public Aspose::Words::CompositeNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | [BuildingBlock](./) sonunu ziyaret etmek için bir ziyaretçi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | [BuildingBlock](./) başlangıcını ziyaret etmek için bir ziyaretçi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_Behavior](./get_behavior/)() const | Blok içeriği ana belgeye eklendiğinde uygulanacak davranışı belirtir. |
| [get_Category](./get_category/)() const | Blok için ikinci düzey sınıflandırmayı belirtir. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_Description](./get_description/)() const | Bu blokla ilişkili açıklamayı alır veya ayarlar. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstSection](./get_firstsection/)() | Bloktaki ilk bölümü alır. |
| [get_Gallery](./get_gallery/)() const | Sınıflandırma veya kullanıcı arayüzü sıralaması amacıyla blok için birinci düzey sınıflandırmayı belirtir. |
| [get_Guid](./get_guid/)() const | Bu bloğu benzersiz şekilde tanımlayan bir tanımlayıcıyı (128 bit GUID) alır veya ayarlar. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastSection](./get_lastsection/)() | Bloktaki son bölümü alır. |
| [get_Name](./get_name/)() const | Bu bloğun adını alır veya ayarlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [BuildingBlock](../../aspose.words/nodetype/) değerini döndürür. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_Sections](./get_sections/)() | Bloktaki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [get_Type](./get_type/)() const | Blok yapı türünü belirtir. |
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
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | Blok içeriği ana belgeye eklendiğinde uygulanacak davranışı belirtir. |
| [set_Category](./set_category/)(const System::String\&) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Category](./get_category/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_Description](./set_description/)(const System::String\&) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Description](./get_description/). |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Gallery](./get_gallery/). |
| [set_Guid](./set_guid/)(System::Guid) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Guid](./get_guid/). |
| [set_Name](./set_name/)(const System::String\&) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | Ayarlayıcı [Aspose::Words::BuildingBlocks::BuildingBlock::get_Type](./get_type/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

Yeni blok yapılarını oluşturabilir ve bir sözlük belgesine ekleyebilirsiniz. Mevcut blok yapılarını değiştirebilir veya silebilirsiniz. Blok yapılarını belgeler arasında kopyalayabilir veya taşıyabilirsiniz. Bir blok yapısının içeriğini bir belgeye ekleyebilirsiniz.

OOXML'deki **docPart**, **docPartPr** ve **docPartBody** öğelerine karşılık gelir.

## Ayrıca Bakınız

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
