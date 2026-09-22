---
title: "Aspose::Words::DocumentBase class"
linktitle: "DocumentBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase sınıfı. Bir Word belgesinin ana belge ve sözlük belgesi için soyut temel sınıfı sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 21000
url: /tr/cpp/aspose.words/documentbase/
---
## DocumentBase class


Bir Word belgesinin ana belge ve sözlük belgesi için soyut temel sınıfı sağlar. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd metodunu çağırır. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart metodunu çağırır. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Belgenin arka plan şekli alınır veya ayarlanır. **null** olabilir. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_Document](./get_document/)() const override | Bu örneği alır. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FontInfos](./get_fontinfos/)() const | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | Belgede tanımlanan dipnot/dipnot ayırıcılarına erişim sağlar. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_Lists](./get_lists/)() const | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_PageColor](./get_pagecolor/)() | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, [BackgroundShape](./get_backgroundshape/) özelliğinin daha basit bir sürümüdür. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [get_Styles](./get_styles/)() const | Belgede tanımlı stillerin bir koleksiyonunu döndürür. |
| [get_WarningCallback](./get_warningcallback/)() const | Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çeşitli belge işleme prosedürleri sırasında çağrılır. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır. |
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
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/) için ayarlayıcı. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Belgede bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/) için ayarlayıcı. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Harici kaynakların nasıl yükleneceğini kontrol etmeye izin verir. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/) için ayarlayıcı. |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Aspose.Words, bir Word belgesini düğüm ağacı olarak temsil eder. [DocumentBase](./), belgenin diğer tüm düğümlerini içeren ağacın kök düğümüdür.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Örnekler



[DocumentBase](./) alt sınıflarının nasıl başlatılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## Ayrıca Bakınız

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
