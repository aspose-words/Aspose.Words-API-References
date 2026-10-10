---
title: "Aspose::Words::Story class"
linktitle: "Story"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story class. Basklass för element som innehåller blocknivå‑noder Paragraph och Table. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 63000
url: /sv/cpp/aspose.words/story/
---
## Story class


Basklass för element som innehåller blocknivå‑noder [Paragraph](../paragraph/) och [Table](../../aspose.words.tables/table/). För att lära dig mer, besök dokumentationsartikeln [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Story : public Aspose::Words::CompositeNode,
              public Aspose::Words::IStory
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepterar en besökare. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXEnd-metoden hos den angivna dokumentbesökaren. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXStart-metoden hos den angivna dokumentbesökaren. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](./appendparagraph/)(const System::String\&) | En genvägsmetod som skapar ett [Paragraph](../paragraph/)‑objekt med valfri text och lägger till det i slutet av detta objekt. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [DeleteShapes](./deleteshapes/)() | Raderar alla former från texten i den här berättelsen. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Hämtar det första stycket i berättelsen. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastParagraph](./get_lastparagraph/)() override | Hämtar det sista stycket i berättelsen. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Hämtar typen av denna nod. |
| [get_Paragraphs](./get_paragraphs/)() override | Hämtar en samling stycken som är omedelbara barn till berättelsen. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_StoryType](./get_storytype/)() override | Hämtar typen av den här storyn. |
| [get_Tables](./get_tables/)() override | Hämtar en samling tabeller som är omedelbara barn till storyn. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetText](../compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
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
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Texten i ett Word‑dokument sägs bestå av flera berättelser. Huvudtexten lagras i huvudtextberättelsen som representeras av [Body](../body/), varje sidhuvud och sidfot lagras i en separat berättelse som representeras av [HeaderFooter](../headerfooter/).

## Exempel



Visar hur man tar bort alla former från en nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
// som har ett föräldra-Paragraph, som är ett barnnod till den första sektionens Body.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Vi kan ta bort alla former från de underordnade styckena i detta Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Se även

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
