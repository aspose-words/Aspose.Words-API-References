---
title: "Aspose::Words::Inline class"
linktitle: "Inbäddad"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Inline class. Basisklass för inline-nivånoder som kan ha teckenformatering associerad med sig, men som inte kan ha egna undernoder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words/inline/
---
## Inline class


Basklass för inline-noder som kan ha teckenformatering associerad med dem, men som inte kan ha egna undernoder. För att lära dig mer, besök dokumentationsartikeln [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) i dokumentationen.

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepterar en besökare. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Hämtar typen av denna nod. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](./get_parentparagraph/)() | Hämtar föräldern [Paragraph](../paragraph/) till denna nod. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../node/remove/)() | Tar bort sig själv från föräldern. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


En klass som härstammar från [Inline](./) kan vara ett barn till [Paragraph](../paragraph/).

## Exempel



Visar hur man bestämmer revideringstypen för en inline-nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// När vi redigerar dokumentet medan alternativet "Track Changes", som finns via Review -> Tracking,
// är aktiverat i Microsoft Word, räknas de ändringar vi gör som revideringar.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revideringar genom att
// anropa dokumentets "StartTrackRevisions"-metod och stoppa spårning genom att använda "StopTrackRevisions"-metoden.
// Vi kan antingen acceptera revisioner för att assimilera dem i dokumentet
// eller avvisa dem för att ändra den föreslagna ändringen effektivt.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Den överordnade noden för en revision är körningen som revisionen gäller. En Run är en Inline-nod.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Nedan är fem typer av revisioner som kan flagga en Inline-nod.
// 1 -  En "insert"-revision:
// Denna revision uppstår när vi infogar text medan vi spårar ändringar.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  En "format"-revision:
// Denna revision uppstår när vi ändrar formateringen av text medan vi spårar ändringar.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  En "move from"-revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// medan vi spårar ändringar visas två revisioner.
// "move from"-revisionen är en kopia av texten som ursprungligen fanns innan vi flyttade den.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  En "move to"-revision:
// "move to"-revisionen är texten som vi flyttade till sin nya position i dokumentet.
// "Move from"- och "move to"-revisioner visas i par för varje flyttrevision vi utför.
// Att acceptera en flyttrevision tar bort "move from"-revisionen och dess text,
// och behåller texten från "move to"-revisionen.
// Att avvisa en flyttrevision behåller däremot "move from"-revisionen och tar bort "move to"-revisionen.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  En "delete"-revision:
// Denna revision uppstår när vi tar bort text medan vi spårar ändringar. När vi tar bort text på detta sätt,
// kommer den att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
// vilket kommer att ta bort texten permanent, eller avvisar revisionen, vilket behåller den text vi tog bort på sin plats.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Se även

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
