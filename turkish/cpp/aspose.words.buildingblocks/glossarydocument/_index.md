---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument class"
linktitle: "GlossaryDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument sınıfı. Bir Word belgesi içinde sözlük belgesinin kök öğesini temsil eder. Sözlük belgesi, AutoText, AutoCorrect girişleri ve Building Blocks için bir depolamadır. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


Bir Word belgesi içinde bir sözlük belgesinin kök öğesini temsil eder. Sözlük belgesi, Otomatik Metin, Otomatik Düzeltme girdileri ve Yapı Blokları için bir depolama alanıdır. Daha fazla bilgi için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class GlossaryDocument : public Aspose::Words::DocumentBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Sözlük belgesinin sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Sözlük belgesinin başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | Belgenin arka plan şekli alınır veya ayarlanır. **null** olabilir. |
| [get_BuildingBlocks](./get_buildingblocks/)() | Sözlük belgesindeki tüm building block'ları temsil eden tiplenmiş bir koleksiyon döndürür. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | Bu örneği alır. |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | Sözlük belgesindeki ilk building block'ı alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | Belgede tanımlanan dipnot/dipnot ayırıcılarına erişim sağlar. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | Sözlük belgesindeki son building block'ı alır. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| [get_NodeType](./get_nodetype/)() const override | [GlossaryDocument](../../aspose.words/nodetype/) değerini döndürür. |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/) özelliğinin daha basit bir sürümüdür. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | Belgede tanımlı stillerin bir koleksiyonunu döndürür. |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çeşitli belge işleme prosedürleri sırasında çağrılır. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String\&, const System::String\&) | Belirtilen galeri, kategori ve adı kullanarak bir building block bulur. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
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
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | [Aspose::Words::DocumentBase::get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/) için ayarlayıcı. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | [Aspose::Words::DocumentBase::get_PageColor](../../aspose.words/documentbase/get_pagecolor/) için ayarlayıcı. |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | [Aspose::Words::DocumentBase::get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/) için ayarlayıcı. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bazı belgeler, genellikle şablonlar, AutoText, AutoCorrect girişlerini ve/veya Building Blocks içerebilir (aynı zamanda *glossary document entries*, *document parts* veya *building blocks* olarak da bilinir).

Yapı taşlarına erişmek için bir belgeyi bir [Document](../../aspose.words/document/) nesnesine yüklemeniz gerekir. Yapı taşları, [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) özelliği aracılığıyla kullanılabilir.

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

OOXML'deki **glossaryDocument** ve **docParts** öğelerine karşılık gelir.

## Ayrıca Bakınız

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
