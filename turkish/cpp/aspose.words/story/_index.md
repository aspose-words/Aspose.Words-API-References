---
title: "Aspose::Words::Story class"
linktitle: "Story"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story class. Blok düzeyinde düğümler Paragraph ve Table içeren öğelerin temel sınıfıdır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 63000
url: /tr/cpp/aspose.words/story/
---
## Story class


Blok düzeyinde düğümler [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) içeren öğelerin temel sınıfı. Daha fazla bilgi için [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) belge makalesini ziyaret edin.

```cpp
class Story : public Aspose::Words::CompositeNode,
              public Aspose::Words::IStory
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd metodunu çağırır. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart metodunu çağırır. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](./appendparagraph/)(const System::String\&) | İsteğe bağlı metinle bir [Paragraph](../paragraph/) nesnesi oluşturan ve bu nesnenin sonuna ekleyen bir kısayol yöntemi. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [DeleteShapes](./deleteshapes/)() | Bu hikayenin metninden tüm şekilleri siler. |
| [get_Count](../compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Hikayedeki ilk paragrafı alır. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastParagraph](./get_lastparagraph/)() override | Hikayedeki son paragrafı alır. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_Paragraphs](./get_paragraphs/)() override | Hikayenin doğrudan çocukları olan paragraf koleksiyonunu alır. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [get_StoryType](./get_storytype/)() override | Bu hikayenin tipini alır. |
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


Bir Word belgesinin metninin birkaç hikayeden oluştuğu söylenir. Ana metin, [Body](../body/) ile temsil edilen ana metin hikayesinde depolanır; her başlık ve altbilgi ise [HeaderFooter](../headerfooter/) ile temsil edilen ayrı bir hikayede depolanır.

## Örnekler



Bir düğümden tüm şekilleri nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil eklemek için DocumentBuilder kullanın. Bu bir satır içi şekildir,
// bu, bir üst Paragraph'a sahiptir ve bu Paragraph, ilk bölümün Body'sunun bir alt düğümüdür.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Bu Body'nin alt paragraflarındaki tüm şekilleri silebiliriz.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ayrıca Bakınız

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
