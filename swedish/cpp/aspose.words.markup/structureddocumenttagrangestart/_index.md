---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart klass"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart klass. Representerar början av ett räckviddsbaserat strukturerat dokumenttagg som accepterar innehåll i flera sektioner. Se även StructuredDocumentTagRangeEnd. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Representerar början av **ranged** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se även [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). För att lära dig mer, besök dokumentationsartikeln [Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till den angivna noden i slutet av stdContent-intervallet. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_Appearance](./get_appearance/)() override | Hämtar eller anger utseendet på den strukturerade dokumenttaggen. |
| [get_Color](./get_color/)() override | Hämtar eller anger färgen på den strukturerade dokumenttaggen. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Id](./get_id/)() override | Anger ett unikt skrivskyddat bestående numeriskt Id för detta strukturerade dokumenttagg. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Anger om innehållet i detta strukturerade dokumenttagg ska tolkas som platshållartext (i motsats till vanligt textinnehåll inom det strukturerade dokumenttagget). Om det är satt till **true** återupptas detta tillstånd (visar platshållartext) när dokumentet öppnas. |
| [get_LastChild](./get_lastchild/)() | Hämtar det sista barnet i stdContent-intervallet. |
| [get_Level](./get_level/)() const override | Hämtar nivån där detta strukturerade dokumenttaggsintervallstart förekommer i dokumentträdet. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | När den är satt till **true** kommer denna egenskap att förhindra en användare från att ta bort detta strukturerade dokumenttagg. |
| [get_LockContents](./get_lockcontents/)() override | När den är satt till **true** kommer denna egenskap att förhindra en användare från att redigera innehållet i detta strukturerade dokumenttagg. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_Placeholder](./get_placeholder/)() override | Hämtar [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext som ska visas när innehållet i detta strukturerade dokumenttaggs‑kör är tomt, det associerade mappade XML‑elementet är tomt enligt vad som anges via [XmlMapping](./get_xmlmapping/)‑elementet eller [IsShowingPlaceholderText](./get_isshowingplaceholdertext/)‑elementet är **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Hämtar eller anger namn på [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_RangeEnd](./get_rangeend/)() | Anger slutet på intervallet om [StructuredDocumentTag](../structureddocumenttag/) är ett intervallbaserat strukturerat dokumenttagg. Annars returneras **null**. |
| [get_SdtType](./get_sdttype/)() override | Hämtar typen av detta strukturerade dokumenttagg. |
| [get_Tag](./get_tag/)() const override | Anger en tagg som är associerad med den aktuella noden för strukturerat dokumenttagg. Kan inte vara **null**. |
| [get_Title](./get_title/)() const override | Anger det vänliga namnet som är associerat med detta strukturerade dokumenttagg. Kan inte vara **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Hämtar en sträng som representerar XML som finns i noden i [FlatOpc](../../aspose.words/saveformat/) formatet. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Hämtar en sträng som representerar XML‑innehållet i noden i [FlatOpc](../../aspose.words/saveformat/)-formatet. Till skillnad från egenskapen [WordOpenXML](./get_wordopenxml/) genererar denna metod ett nedskalat dokument som utesluter alla icke‑innehållsrelaterade delar. |
| [get_XmlMapping](./get_xmlmapping/)() override | Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggsintervall till XML‑data i en anpassad XML‑del av det aktuella dokumentet. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Returnerar en levande samling av undernoder som matchar de angivna typerna. |
| [GetEnumerator](./getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](./removeallchildren/)() | Tar bort alla noder mellan detta intervallstartnod och intervallslutnod. |
| [RemoveSelfOnly](./removeselfonly/)() override | Tar bort detta intervallstart‑ och motsvarande intervallslutnod för det strukturerade dokumenttagget, men behåller dess innehåll i dokumentträdet. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Initierar en ny instans av klassen **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får egenskaperna för strukturerade dokumenttaggar med flera sektioner.
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

## Se även

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
