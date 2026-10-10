---
title: "Aspose::Words::EditableRangeEnd sınıfı"
linktitle: "Düzenlenebilir bir aralığın sonu."
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRangeEnd sınıfı. Word belgesinde düzenlenebilir bir aralığın sonunu temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 25000
url: /tr/cpp/aspose.words/editablerangeend/
---
## EditableRangeEnd class


Bir Word belgesindeki düzenlenebilir bir aralığın sonunu temsil eder. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class EditableRangeEnd : public Aspose::Words::Node,
                         public Aspose::Words::IDisplaceableByCustomXml,
                         public Aspose::Words::INodeWithAnnotationId
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_EditableRangeStart](./get_editablerangestart/)() | İlgili [EditableRangeStart](../editablerangestart/), ID ile alınan. |
| [get_Id](./get_id/)() const | Düzenlenebilir aralığın tanımlayıcısını belirtir. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [EditableRangeEnd](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
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
| [set_Id](./set_id/)(int32_t) | Ayarlayıcı [Aspose::Words::EditableRangeEnd::get_Id](./get_id/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Word belgesindeki tam bir düzenlenebilir aralık, aynı Id'ye sahip bir [EditableRangeStart](./get_editablerangestart/) ve eşleşen bir [EditableRangeEnd](./) içerir.

[EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./) are just markers inside a document that specify where the editable range starts and ends.

Düzenlenebilir bir aralıkla tek bir nesne olarak çalışmak için [EditableRange](../editablerange/) sınıfını bir "fasad" olarak kullanın.


Şu anda düzenlenebilir aralıklar yalnızca satır içi seviyesinde desteklenir, yani [Paragraph](../paragraph/) içinde, ancak düzenlenebilir aralık başlangıcı ve düzenlenebilir aralık sonu farklı paragraflarda olabilir.

## Ayrıca Bakınız

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
