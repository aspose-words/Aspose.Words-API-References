---
title: "Aspose::Words::Fields::FieldEnd sınıfı"
linktitle: "FieldEnd"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldEnd sınıfı. Bir belgede Word alanının sonunu temsil eder. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 39000
url: /tr/cpp/aspose.words.fields/fieldend/
---
## FieldEnd class


Bir belgedeki Word alanının sonunu temsil eder. Daha fazla bilgi edinmek için, [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldEnd : public Aspose::Words::Fields::FieldChar
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Alan tipini döndürür. |
| [get_Font](../../aspose.words/inline/get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_HasSeparator](./get_hasseparator/)() const | Bu alan bir ayırıcıya sahipse **true** döndürür. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Üst alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplamamalıdır). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [FieldEnd](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../../aspose.words/paragraph/) öğesini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Alan karakteri için bir alan döndürür. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Bu düğümün temsil ettiği özel karakteri alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[FieldEnd](./) is an inline-level node and represented by the [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) control character in the document.

[FieldEnd](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

Microsoft Word belgesindeki tam bir alan, alan başlangıç karakteri, alan kodu, alan ayırıcı karakteri, alan sonucu ve alan bitiş karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan bitişi bulunur.

Yeni bir alanı belgeye kolayca eklemek için [InsertField()](../) yöntemini kullanın.
## Ayrıca Bakınız

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
