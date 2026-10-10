---
title: "Aspose::Words::Fields::FieldChar sınıfı"
linktitle: "FieldChar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldChar sınıfı. Bir belgede alan karakterlerini temsil eden düğümler için temel sınıftır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.fields/fieldchar/
---
## FieldChar class


Bir belgede alan karakterlerini temsil eden düğümler için temel sınıf. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldChar : public Aspose::Words::SpecialChar
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](../../aspose.words/specialchar/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FieldType](./get_fieldtype/)() const | Alan tipini döndürür. |
| [get_Font](../../aspose.words/inline/get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsDirty](./get_isdirty/)() const | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsLocked](./get_islocked/)() const | Üst alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplamamalıdır). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](../../aspose.words/specialchar/get_nodetype/)() const override | [SpecialChar](../../aspose.words/nodetype/) döndürür. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../../aspose.words/paragraph/) öğesini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](./getfield/)() | Alan karakteri için bir alan döndürür. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Bu düğümün temsil ettiği özel karakteri alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_IsDirty](./set_isdirty/)(bool) | [Aspose::Words::Fields::FieldChar::get_IsDirty](./get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](./set_islocked/)(bool) | [Aspose::Words::Fields::FieldChar::get_IsLocked](./get_islocked/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word belgesindeki tam bir alan, alan başlangıç karakteri, alan kodu, alan ayırıcı karakteri, alan sonucu ve alan bitiş karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan bitişi bulunur.

Yeni bir alanı belgeye kolayca eklemek için [InsertField()](../) yöntemini kullanın.

## Örnekler



[FieldStart](../fieldstart/) düğümüyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Belge içindeki alanı temsil eden facade nesnesini alın.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Alanı güncel tarihi gösterecek şekilde güncelleyin.
field->Update();
```

## Ayrıca Bakınız

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
