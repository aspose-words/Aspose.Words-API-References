---
title: "Aspose::Words::DocumentBase klass"
linktitle: "DocumentBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase klass. Tillhandahåller den abstrakta basklassen för ett huvuddokument och ett glossariedokument i ett Word‑dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words/documentbase/
---
## DocumentBase class


Tillhandahåller den abstrakta basklassen för ett huvuddokument och ett glossaridokument i ett Word-dokument. För att läsa mer, besök artikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepterar en besökare. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXEnd-metoden hos den angivna dokumentbesökaren. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXStart-metoden hos den angivna dokumentbesökaren. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Hämtar eller anger bakgrundsformen för dokumentet. Kan vara **null**. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_Document](./get_document/)() const override | Hämtar denna instans. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FontInfos](./get_fontinfos/)() const | Tillhandahåller åtkomst till egenskaper för teckensnitt som används i detta dokument. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | Tillhandahåller åtkomst till fotnot-/slutnotseparatorerna som definierats i dokumentet. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_Lists](./get_lists/)() const | Tillhandahåller åtkomst till listformateringen som används i dokumentet. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Kallas när en nod infogas eller tas bort i dokumentet. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Hämtar typen av denna nod. |
| [get_PageColor](./get_pagecolor/)() | Hämtar eller anger sidans färg i dokumentet. Denna egenskap är en enklare version av [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Tillåter att styra hur externa resurser laddas. |
| [get_Styles](./get_styles/)() const | Returnerar en samling av stilar som definierats i dokumentet. |
| [get_WarningCallback](./get_warningcallback/)() const | Kallas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan leda till förlust av data‑ eller formateringsnoggrannhet. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetText](../compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Tar bort alla barnnoder för den aktuella noden. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../../aspose.words.markup/smarttag/)‑nedärvda noder för den aktuella noden. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../node/) som matchar XPath‑uttrycket. |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Sättare för [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Kallas när en nod infogas eller tas bort i dokumentet. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att styra hur externa resurser laddas. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Sättare för [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Aspose.Words representerar ett Word‑dokument som ett träd av noder. [DocumentBase](./) är en rot‑nod i trädet som innehåller alla andra noder i dokumentet.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Exempel



Visar hur man initierar underklasserna till [DocumentBase](./).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## Se även

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
