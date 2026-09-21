---
title: "Aspose::Words::Markup::StructuredDocumentTag-klass"
linktitle: "StructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag-klass. Representerar en strukturerad dokumenttagg (SDT eller innehållskontroll) i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Representerar en strukturerad dokumenttagg (SDT eller innehållskontroll) i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Rensar innehållet i denna strukturerade dokumenttagg och visar en platshållare om den är definierad. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_Appearance](./get_appearance/)() override | Hämtar/sätter utseendet på en strukturerad dokumenttagg. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Anger kategori för byggblock för denna **SDT**-nod. Kan inte vara **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Anger typ av byggblock för denna **SDT**. Kan inte vara **null**. |
| [get_CalendarType](./get_calendartype/)() | Anger kalendertypen för denna **SDT**. Standard är [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Hämtar/sätter aktuellt tillstånd för kryssrutan **SDT**. Standardvärdet för denna egenskap är **false**. |
| [get_Color](./get_color/)() override | Hämtar eller anger färgen på den strukturerade dokumenttaggen. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) formatering som kommer att tillämpas på text som matas in i **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Sträng som representerar formatet i vilket datum visas. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Tillåter att ange/hämta språkformatet för datumet som visas i detta **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Hämtar/anger formatet i vilket datumet för en datum‑SDT lagras när **SDT** är bunden till en XML‑nod i dokumentets datalager. Standardvärdet är [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) formatering som kommer att tillämpas på det sista tecknet i text som matas in i **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FullDate](./get_fulldate/)() | Anger det fullständiga datum och tid som senast matades in i detta **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_Id](./get_id/)() override | Anger ett unikt skrivskyddat bestående numeriskt Id för denna **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Anger om innehållet i detta **SDT** ska tolkas som att det innehåller platshållartext (i motsats till vanlig textinnehåll i SDT). om den är satt till **true** återupptas detta tillstånd (visar platshållartext) när dokumentet öppnas. |
| [get_IsTemporary](./get_istemporary/)() const | Anger om detta **SDT** ska tas bort från WordProcessingML‑dokumentet när dess innehåll ändras. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_Level](./get_level/)() const override | Hämtar nivån där denna **SDT** förekommer i dokumentträdet. |
| [get_ListItems](./get_listitems/)() | Hämtar [SdtListItemCollection](../sdtlistitemcollection/) som är associerad med detta **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | När den är satt till **true** kommer denna egenskap att förhindra en användare från att ta bort detta **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | När den är satt till **true** kommer denna egenskap att förhindra en användare från att redigera innehållet i detta **SDT**. |
| [get_Multiline](./get_multiline/)() | Anger om detta **SDT** tillåter flera textrader. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_Placeholder](./get_placeholder/)() override | Hämtar [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext som ska visas när innehållet i detta SDT‑kör är tomt, den associerade mappade XML‑elementet är tomt enligt [XmlMapping](./get_xmlmapping/)-elementet eller [IsShowingPlaceholderText](./get_isshowingplaceholdertext/)-elementet är **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Hämtar eller anger namn på [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_SdtType](./get_sdttype/)() override | Hämtar typ av denna **Structured document tag**. |
| [get_Style](./get_style/)() | Hämtar eller anger [Style](../../aspose.words/style/) för den strukturerade dokumenttaggen. |
| [get_StyleName](./get_stylename/)() | Hämtar eller anger namnet på stilen som tillämpas på den strukturerade dokumenttaggen. |
| [get_Tag](./get_tag/)() const override | Anger en tagg som är associerad med den aktuella SDT‑noden. Kan inte vara **null**. |
| [get_Title](./get_title/)() const override | Anger det vänliga namnet som är associerat med detta **SDT**. Kan inte vara **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Hämtar en sträng som representerar XML som finns i noden i [FlatOpc](../../aspose.words/saveformat/) formatet. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Hämtar en sträng som representerar XML‑innehållet i noden i [FlatOpc](../../aspose.words/saveformat/)-formatet. Till skillnad från egenskapen [WordOpenXML](./get_wordopenxml/) genererar denna metod ett nedskalat dokument som utesluter alla icke‑innehållsrelaterade delar. |
| [get_XmlMapping](./get_xmlmapping/)() override | Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttagg till XML-data i en anpassad XML-del av det aktuella dokumentet. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla barnnoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../smarttag/)-nedärvda noder från den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../../aspose.words/node/) som matchar XPath‑uttrycket. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Sättare för [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Anger symbolen som används för att representera det markerade tillståndet för en kryssrutan innehållskontroll. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Anger symbolen som används för att representera det avmarkerade tillståndet för en kryssrutan innehållskontroll. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Initierar en ny instans av klassen **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Strukturerade dokumenttaggar (SDT) gör det möjligt att bädda in kunddefinierad semantik samt dess beteende och utseende i ett dokument.

I den här versionen erbjuder Aspose.Words ett antal offentliga metoder och egenskaper för att manipulera beteendet och innehållet i [StructuredDocumentTag](./). Mappning av SDT‑noder till anpassade XML‑paket i ett dokument kan utföras med hjälp av egenskapen [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Exempel



Visar hur man arbetar med stilar för innehållskontrollelement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två sätt att applicera en stil från dokumentet på en strukturerad dokumenttagg.
// 1 -  Applicera ett stilobjekt från dokumentets stilkollektion:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Referera till en stil i dokumentet med namn:
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

## Se även

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
