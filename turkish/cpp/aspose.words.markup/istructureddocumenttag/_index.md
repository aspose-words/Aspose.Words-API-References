---
title: "Aspose::Words::Markup::IStructuredDocumentTag arayüzü"
linktitle: "IStructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag arayüzü. C++'da StructuredDocumentTag ve StructuredDocumentTagRangeStart için ortak veri tanımlamak amacıyla kullanılan bir arayüz."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


[StructuredDocumentTag](../structureddocumenttag/) ve [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) için ortak veri tanımlayan bir arayüz.

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar. |
| virtual [get_Color](./get_color/)() | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| virtual [get_Id](./get_id/)() | Bu **SDT** için benzersiz, yalnızca okunabilir, kalıcı sayısal kimliği belirtir. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise true döndürür. |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Bu **SDT** içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriğine karşı) yorumlanıp yorumlanmayacağını belirtir. true olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metni göstererek) yeniden etkinleştirilir. |
| virtual [get_Level](./get_level/)() const | Bu **SDT**'nin belge ağacında bulunduğu seviyeyi alır. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | True olarak ayarlandığında, bu özellik kullanıcının bu **SDT**'yi silmesini engeller. |
| virtual [get_LockContents](./get_lockcontents/)() | True olarak ayarlandığında, bu özellik kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller. |
| virtual [get_Node](./get_node/)() | Bu arayüzü uygulayan [Node](../../aspose.words/node/) nesnesini döndürür. |
| virtual [get_Placeholder](./get_placeholder/)() | Bu SDT çalıştırma içeriği boş olduğunda, ilişkili eşlenmiş XML öğesi [XmlMapping](./get_xmlmapping/) öğesiyle belirtilen şekilde boş olduğunda veya [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) öğesi true olduğunda görüntülenmesi gereken yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesini alır. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesinin adını alır veya ayarlar. |
| virtual [get_SdtType](./get_sdttype/)() | Bu **Structured document tag** tipini alır. |
| virtual [get_Tag](./get_tag/)() const | Mevcut SDT düğümüyle ilişkili bir etiketi belirtir. Null olamaz. |
| virtual [get_Title](./get_title/)() const | Bu **SDT** ile ilişkili dostane adı belirtir. Null olamaz. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Düğüm içinde bulunan XML'i [FlatOpc](../../aspose.words/saveformat/) biçiminde temsil eden bir dizeyi alır. |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Bu yapılandırılmış belge etiketinin, mevcut belgenin özel bir XML bölümündeki XML verilerine eşlenmesini temsil eden bir nesneyi alır. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Bu SDT düğümünü yalnızca kendisini kaldırır, ancak içeriğini belge ağacında tutar. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/) için ayarlayıcı. |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/) için ayarlayıcı. |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/) için ayarlayıcı. |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/) için ayarlayıcı. |
| virtual [set_LockContents](./set_lockcontents/)(bool) | [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/) için ayarlayıcı. |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/) için ayarlayıcı. |
| virtual [set_Tag](./set_tag/)(System::String) | [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/) için ayarlayıcı. |
| virtual [set_Title](./set_title/)(System::String) | Ayarlayıcı for [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Örnekler



Yapılandırılmış belge etiketini nasıl kaldıracağını gösterir, ancak içindeki içeriği korur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Bu koleksiyon, aralıklı ve aralıklı olmayan yapılandırılmış etiketlere erişim için birleşik bir arayüz sağlar.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Burada, aralıklı ve aralıklı olmayan yapılandırılmış etiketlerin ortak arayüzünden alt düğümleri alabiliriz.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
