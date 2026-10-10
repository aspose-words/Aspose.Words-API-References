---
title: "Aspose::Words::CommentRangeStart class"
linktitle: "CommentRangeStart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CommentRangeStart class. Anger början på ett textområde som har en kommentar kopplad till sig. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/commentrangestart/
---
## CommentRangeStart class


Anger början på ett textområde som har en kommentar kopplad till sig. För att läsa mer, besök dokumentationsartikeln [Arbeta med kommentarer](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentRangeStart : public Aspose::Words::Node,
                          public Aspose::Words::IDisplaceableByCustomXml,
                          public Aspose::Words::INodeWithAnnotationId
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [CommentRangeStart](./commentrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | Initierar en ny instans av den här klassen. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Id](./get_id/)() const | Anger identifieraren för kommentaren som detta område är länkat till. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [CommentRangeStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
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
| [set_Id](./set_id/)(int32_t) | Anger identifieraren för kommentaren som detta område är länkat till. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


För att skapa en kommentar förankrad i ett textområde måste du skapa en [Comment](../comment/) och sedan skapa [CommentRangeStart](./) och [CommentRangeEnd](../commentrangeend/) och sätta deras identifierare till samma [Id](../comment/get_id/) värde.

[CommentRangeStart](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

## Se även

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
