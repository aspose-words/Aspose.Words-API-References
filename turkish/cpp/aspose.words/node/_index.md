---
title: "Aspose::Words::Node sınıfı"
linktitle: "Node"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node sınıfı. Word belgesindeki tüm düğümler için temel sınıf. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 41000
url: /tr/cpp/aspose.words/node/
---
## Node class


Bir Word belgesinin tüm düğümleri için temel sınıftır. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class Node : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| [Clone](./clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](./get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](./get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| virtual [get_IsComposite](./get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_NextNode](./get_nextnode/)() const |  |
| [get_NextSibling](./get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](./get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_ParentNode](./get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreviousSibling](./get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](./get_prevnode/)() const |  |
| [get_Range](./get_range/)() | Bu düğüm içinde bulunan belgenin bir bölümünü temsil eden bir [Range](../range/) nesnesi döndürür. |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../nodetype/) öğesinin ilk atasını alır. |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](./isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](./remove/)() | Kendisini üst düğümden kaldırır. |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | Ayarlayıcı [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/) için. |
| [set_NextNode](./set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](./set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](./setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir belge, DOM veya XmlDocument'e benzer şekilde düğümlerin bir ağacı olarak temsil edilir.

Daha fazla bilgi için Composite tasarım desenine bakın.

Bu [Node](./) sınıfı:

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## Örnekler



Bir birleşik düğümün nasıl kopyalanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Aşağıda bir birleşik düğümün kopyalanmasının iki yolu verilmiştir.
// 1 -  Bir düğümün bir kopyasını oluştur ve aynı zamanda onun tüm alt düğümlerinin de bir kopyasını oluştur.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Bir düğümün yalnızca kendisinin bir kopyasını, alt düğüm olmadan oluştur.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```


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


Bir birleşik düğümden belirli bir türdeki tüm alt düğümleri nasıl kaldıracağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Bu düğümü sildikten sonra ona geçmek isteyebileceğimiz durum için sonraki kardeş düğümü bir değişken olarak kaydet.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Bir bölüm gövdesi Paragraph ve Table düğümlerini içerebilir.
    // Düğüm bir Tablo ise, onu üst öğeden kaldır.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
