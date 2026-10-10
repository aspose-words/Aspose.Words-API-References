---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart class"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart sınıfı. Çok bölümlü içeriği kabul eden aralıklı yapılandırılmış belge etiketinin başlangıcını temsil eder. Ayrıca StructuredDocumentTagRangeEnd bölümüne bakın. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Çok bölümlü içeriği kabul eden **ranged** yapılandırılmış belge etiketinin başlangıcını temsil eder. Ayrıca [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/) bölümüne bakın. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) belge makalesini ziyaret edin.

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümü stdContent aralığının sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_Appearance](./get_appearance/)() override | Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar. |
| [get_Color](./get_color/)() override | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Id](./get_id/)() override | Bu yapılandırılmış belge etiketi için benzersiz, yalnızca okunabilir, kalıcı sayısal bir kimlik belirtir. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Bu yapılandırılmış belge etiketinin içeriğinin yer tutucu metin içerdiği (yapılandırılmış belge etiketindeki normal metin içeriğine karşı) yorumlanıp yorumlanmayacağını belirtir. **true** olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metin gösterilerek) yeniden başlatılır. |
| [get_LastChild](./get_lastchild/)() | stdContent aralığındaki son çocuğu alır. |
| [get_Level](./get_level/)() const override | Bu yapılandırılmış belge etiketi aralığı başlangıcının belge ağacında oluştuğu seviyeyi alır. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | **true** olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller. |
| [get_LockContents](./get_lockcontents/)() override | **true** olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_Placeholder](./get_placeholder/)() override | Bu yapılandırılmış belge etiketi çalıştırma içeriği boş olduğunda, ilişkili eşlenmiş XML öğesi [XmlMapping](./get_xmlmapping/) öğesi aracılığıyla belirtilen şekilde boş olduğunda veya [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) öğesi **true** olduğunda gösterilmesi gereken yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesini alır. |
| [get_PlaceholderName](./get_placeholdername/)() override | Yer tutucu metni içeren [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) öğesinin adını alır veya ayarlar. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_RangeEnd](./get_rangeend/)() | Eğer [StructuredDocumentTag](../structureddocumenttag/) bir aralıklı yapılandırılmış belge etiketi ise aralığın sonunu belirtir. Aksi takdirde **null** döndürür. |
| [get_SdtType](./get_sdttype/)() override | Bu yapılandırılmış belge etiketinin tipini alır. |
| [get_Tag](./get_tag/)() const override | Mevcut yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. **null** olamaz. |
| [get_Title](./get_title/)() const override | Bu yapılandırılmış belge etiketiyle ilişkili dostane adı belirtir. **null** olamaz. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Düğüm içinde bulunan XML'i [FlatOpc](../../aspose.words/saveformat/) biçiminde temsil eden bir dizeyi alır. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Düğüm içinde bulunan XML'i [FlatOpc](../../aspose.words/saveformat/) biçiminde temsil eden bir dize alır. [WordOpenXML](./get_wordopenxml/) özelliğinin aksine, bu yöntem içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur. |
| [get_XmlMapping](./get_xmlmapping/)() override | Bu yapılandırılmış belge etiketi aralığının mevcut belgenin özel bir XML bölümündeki XML verilerine eşlenmesini temsil eden bir nesneyi alır. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](./removeallchildren/)() | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır. |
| [RemoveSelfOnly](./removeselfonly/)() override | Bu yapılandırılmış belge etiketinin bu aralık başlangıç ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacında tutar. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/) için ayarlayıcı. |
| [set_Color](./set_color/)(System::Drawing::Color) override | [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/) için ayarlayıcı. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/) için ayarlayıcı. |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/) için ayarlayıcı. |
| [set_LockContents](./set_lockcontents/)(bool) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Ayarlayıcı [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Yeni bir **Structured document tag range start** sınıfı örneği başlatır. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |

## Örnekler



Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Ayrıca Bakınız

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
