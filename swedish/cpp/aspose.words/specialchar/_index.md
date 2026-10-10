---
title: "Aspose::Words::SpecialChar class"
linktitle: "SpecialChar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SpecialChar class. Basklass för specialtecken i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 62000
url: /sv/cpp/aspose.words/specialchar/
---
## SpecialChar class


Basisklass för specialtecken i dokumentet. För att läsa mer, besök [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokumentationsartikel.

```cpp
class SpecialChar : public Aspose::Words::Inline
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Font](../inline/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [SpecialChar](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Hämtar föräldern [Paragraph](../paragraph/) till denna nod. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Hämtar det speciella tecknet som denna nod representerar. |
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


Ett Microsoft Word-dokument kan innehålla ett antal specialtecken som representerar fält, formulärfält, former, OLE-objekt, fotnoter etc. För listan över specialtecken, se [ControlChar](../controlchar/).

[SpecialChar](./) is an inline-node and can only be a child of [Paragraph](../paragraph/).

[SpecialChar](./) char is used as a base class for more specific classes that represent special characters that Aspose.Words provides programmatic access for. The [SpecialChar](./) class is also used itself to represent special character for which Aspose.Words does not provide detailed programmatic access. 
## Se även

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
