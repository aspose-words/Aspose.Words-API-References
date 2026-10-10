---
title: "Aspose::Words::CompositeNode class"
linktitle: "CompositeNode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode class. Diğer düğümleri içerebilen düğümler için temel sınıftır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 15000
url: /tr/cpp/aspose.words/compositenode/
---
## CompositeNode class


Diğer düğümleri içerebilen düğümler için temel sınıftır. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class CompositeNode : public Aspose::Words::Node,
                      public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                      public Aspose::Words::INodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| virtual [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd metodunu çağırır. |
| virtual [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart metodunu çağırır. |
| [AppendChild](./appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_Count](./get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](./get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_HasChildNodes](./get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_IsComposite](./get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastChild](./get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](./getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](./gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](./insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](./insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](./prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](./removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](./removechild/)(T) |  |
| [RemoveSmartTags](./removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](./selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](./selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../node/) öğesini seçer. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir belge, DOM veya XmlDocument'e benzer şekilde düğümlerin bir ağacı olarak temsil edilir.

Daha fazla bilgi için Composite tasarım desenine bakın.

[CompositeNode](./) sınıfı:

* Provides access to the child nodes.
* Implements Composite operations such as insert and remove children.
* Provides methods for XPath navigation.



## Örnekler



Bir birleşik düğümün alt düğüm koleksiyonunda nasıl gezileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bu belgenin ilk paragrafına iki koşu ve bir şekil alt düğüm olarak ekle.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Not: 'CustomNodeId' bir çıktı dosyasına kaydedilmez ve yalnızca düğüm ömrü boyunca vardır.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Paragrafın doğrudan alt eleman koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz tüm run'ları veya şekilleri yazdırın.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Ayrıca Bakınız

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
