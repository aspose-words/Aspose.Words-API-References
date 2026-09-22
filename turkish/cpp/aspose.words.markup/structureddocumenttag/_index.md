---
title: "Aspose::Words::Markup::StructuredDocumentTag sınıfı"
linktitle: "StructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag sınıfı. Bir belgede yapılandırılmış belge etiketi (SDT veya içerik kontrolü) temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Bir belgede yapılandırılmış belge etiketi (SDT veya içerik kontrolü) temsil eder. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi, [StructuredDocumentTag](./) sonunu ziyaret etmek için kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi, [StructuredDocumentTag](./) başlangıcını ziyaret etmek için kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlıysa bir yer tutucu gösterir. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_Appearance](./get_appearance/)() override | Bir yapılandırılmış belge etiketinin görünümünü alır/ayarlar. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | **SDT** düğümü için yapı bloğu kategorisini belirtir. **null** olamaz. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Bu **SDT** için yapı bloğu tipini belirtir. **null** olamaz. |
| [get_CalendarType](./get_calendartype/)() | Bu **SDT** için takvim tipini belirtir. Varsayılan [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Onay kutusu **SDT**'nin mevcut durumunu alır/ayarlar. Bu özelliğin varsayılan değeri **false**. |
| [get_Color](./get_color/)() override | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) biçimlendirmesi, **SDT** içine girilen metne uygulanacaktır. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Tarihlerin görüntülendiği biçimi temsil eden dize. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Bu **SDT** içinde görüntülenen tarihin dil biçimini ayarlamaya/alma izni verir. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Bir tarih SDT'si için tarihin, **SDT** belge veri deposundaki bir XML düğümüne bağlandığında saklandığı biçimi alır/ayarlar. Varsayılan değer [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) biçimlendirmesi, **SDT** içine girilen metnin son karakterine uygulanacaktır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FullDate](./get_fulldate/)() | Bu **SDT**'ye son girilen tam tarih ve saati belirtir. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_Id](./get_id/)() override | Bu **SDT** için benzersiz, yalnızca okunabilir, kalıcı sayısal kimliği belirtir. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Bu **SDT**'nin içeriğinin yer tutucu metin içerdiği (SDT içindeki normal metin içeriğine karşı) yorumlanıp yorumlanmayacağını belirtir. **true** olarak ayarlanırsa, bu durum (yer tutucu metin gösterilerek) belge açıldığında devam eder. |
| [get_IsTemporary](./get_istemporary/)() const | Bu **SDT**'nin içeriği değiştirildiğinde WordProcessingML belgesinden kaldırılıp kaldırılmayacağını belirtir. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_Level](./get_level/)() const override | Bu **SDT**'nin belge ağacında bulunduğu seviyeyi alır. |
| [get_ListItems](./get_listitems/)() | Bu **SDT** ile ilişkili [SdtListItemCollection](../sdtlistitemcollection/) alır. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | **true** olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'yi silmesini engeller. |
| [get_LockContents](./get_lockcontents/)() override | **true** olarak ayarlandığında, bu özellik bir kullanıcının bu **SDT**'nin içeriğini düzenlemesini engeller. |
| [get_Multiline](./get_multiline/)() | Bu **SDT**'nin birden fazla satır metin içermesine izin verip vermediğini belirtir. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_Placeholder](./get_placeholder/)() override | Bu SDT çalıştırma içeriği boş olduğunda, ilişkili eşlenmiş XML öğesi [XmlMapping](./get_xmlmapping/) öğesi aracılığıyla belirtilen şekilde boş olduğunda veya [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) öğesi **true** olduğunda gösterilmesi gereken yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesini alır. |
| [get_PlaceholderName](./get_placeholdername/)() override | Yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesinin adını alır veya ayarlar. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_SdtType](./get_sdttype/)() override | Bu **Structured document tag** tipini alır. |
| [get_Style](./get_style/)() | Yapılandırılmış belge etiketinin [Style](../../aspose.words/style/) değerini alır veya ayarlar. |
| [get_StyleName](./get_stylename/)() | Yapılandırılmış belge etiketine uygulanan stilin adını alır veya ayarlar. |
| [get_Tag](./get_tag/)() const override | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. **null** olamaz. |
| [get_Title](./get_title/)() const override | Bu **SDT** ile ilişkili dostane adı belirtir. **null** olamaz. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Düğüm içinde bulunan XML'i [FlatOpc](../../aspose.words/saveformat/) biçiminde temsil eden bir dizeyi alır. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Düğüm içinde bulunan XML'i [FlatOpc](../../aspose.words/saveformat/) biçiminde temsil eden bir dize alır. [WordOpenXML](./get_wordopenxml/) özelliğinin aksine, bu yöntem içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur. |
| [get_XmlMapping](./get_xmlmapping/)() override | Bu yapılandırılmış belge etiketinin, mevcut belgenin özel bir XML bölümündeki XML verilerine eşlenmesini temsil eden bir nesneyi alır. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Bu SDT düğümünü yalnızca kendisini kaldırır, ancak içeriğini belge ağacında tutar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../../aspose.words/node/) öğesini seçer. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/) için ayarlayıcı. |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/) için ayarlayıcı. |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/) için ayarlayıcı. |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/) için ayarlayıcı. |
| [set_Checked](./set_checked/)(bool) | [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/) için ayarlayıcı. |
| [set_Color](./set_color/)(System::Drawing::Color) override | [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/) için ayarlayıcı. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/) için ayarlayıcı. |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/) için ayarlayıcı. |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/) için ayarlayıcı. |
| [set_FullDate](./set_fulldate/)(System::DateTime) | [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/) için ayarlayıcı. |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/) için ayarlayıcı. |
| [set_IsTemporary](./set_istemporary/)(bool) | [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/) için ayarlayıcı. |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/) için ayarlayıcı. |
| [set_LockContents](./set_lockcontents/)(bool) override | [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/) için ayarlayıcı. |
| [set_Multiline](./set_multiline/)(bool) | [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/) için ayarlayıcı. |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | İşaret kutusu içerik denetiminin işaretli durumunu temsil eden sembolü ayarlar. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | İşaret kutusu içerik denetiminin işaretsiz durumunu temsil eden sembolü ayarlar. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Yeni bir **Structured document tag** sınıfı örneği başlatır. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Yapılandırılmış belge etiketleri (SDT'ler), müşteri tanımlı anlamsallığı, davranışını ve görünümünü bir belgeye gömmeyi sağlar.

Bu sürümde Aspose.Words, [StructuredDocumentTag](./) davranışını ve içeriğini manipüle etmek için bir dizi genel yöntem ve özellik sağlar. Bir belgede SDT düğümlerinin özel XML paketlerine eşlenmesi, [XmlMapping](./get_xmlmapping/) özelliği kullanılarak gerçekleştirilebilir.

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Örnekler



İçerik denetimi öğeleri için stillerle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda bir belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 -  Belgenin stil koleksiyonundan bir stil nesnesi uygula:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Belgedeki bir stili adını kullanarak referansla:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## Ayrıca Bakınız

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
