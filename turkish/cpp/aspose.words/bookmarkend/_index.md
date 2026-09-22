---
title: "Aspose::Words::BookmarkEnd class"
linktitle: "Bir yer imi işaretleyicisinin sonu."
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BookmarkEnd sınıfı. Bir Word belgesindeki yer işaretinin sonunu temsil eder. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/bookmarkend/
---
## BookmarkEnd class


Bir Word belgesindeki yer iminin sonunu temsil eder. Daha fazla bilgi için, [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) dokümantasyon makalesini ziyaret edin.

```cpp
class BookmarkEnd : public Aspose::Words::Node,
                    public Aspose::Words::IBookmarkNode,
                    public Aspose::Words::IDisplaceableByCustomXml
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [BookmarkEnd](./bookmarkend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | [BookmarkEnd](./) sınıfının yeni bir örneğini başlatır. |
| [Clone](../node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_Name](./get_name/)() override | Yer imi adını alır. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [BookmarkEnd](../nodetype/) döndürür. |
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
| [set_Name](./set_name/)(System::String) override | Yer imi adını ayarlar. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir Word belgesindeki tam bir yer işareti, aynı yer işareti adına sahip bir [BookmarkStart](../bookmarkstart/) ve eşleşen bir [BookmarkEnd](./) içerir.

[BookmarkStart](../bookmarkstart/) and [BookmarkEnd](./) are just markers inside a document that specify where the bookmark starts and ends.

Yer işaretiyle tek bir nesne olarak çalışmak için [Bookmark](../bookmark/) sınıfını bir "facade" olarak kullanın.
## Ayrıca Bakınız

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
