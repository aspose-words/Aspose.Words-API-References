---
title: "Aspose::Words::EditableRangeStart class"
linktitle: "Düzenlenebilir bir aralığın başlangıcı."
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRangeStart sınıfı. Word belgesinde düzenlenebilir bir aralığın başlangıcını temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 26000
url: /tr/cpp/aspose.words/editablerangestart/
---
## EditableRangeStart class


Bir Word belgesindeki düzenlenebilir bir aralığın başlangıcını temsil eder. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class EditableRangeStart : public Aspose::Words::Node,
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
| [get_EditableRange](./get_editablerange/)() | Bu düzenlenebilir aralık başlangıcı ve sonunu kapsayan dış görünüm nesnesini alır. |
| [get_Id](./get_id/)() const | Düzenlenebilir aralığın tanımlayıcısını belirtir. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [EditableRangeStart](../nodetype/). |
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
| [set_Id](./set_id/)(int32_t) | [Aspose::Words::EditableRangeStart::get_Id](./get_id/) için ayarlayıcı. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Word belgesindeki tam bir düzenlenebilir aralık, aynı Id'ye sahip bir [EditableRangeStart](./) ve eşleşen bir [EditableRangeEnd](../editablerangeend/) içerir.

[EditableRangeStart](./) and [EditableRangeEnd](../editablerangeend/) are just markers inside a document that specify where the editable range starts and ends.

[EditableRange](./get_editablerange/) sınıfını bir "facade" olarak kullanarak düzenlenebilir bir aralıkla tek bir nesne gibi çalışın.


Şu anda düzenlenebilir aralıklar yalnızca satır içi seviyesinde desteklenir, yani [Paragraph](../paragraph/) içinde, ancak düzenlenebilir aralık başlangıcı ve düzenlenebilir aralık sonu farklı paragraflarda olabilir.

## Ayrıca Bakınız

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
