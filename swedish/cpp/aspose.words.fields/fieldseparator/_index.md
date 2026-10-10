---
title: "Aspose::Words::Fields::FieldSeparator class"
linktitle: "FieldSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSeparator-klass. Representerar en Word-fältseparator som separerar fältkoden från fältresultatet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 90000
url: /sv/cpp/aspose.words.fields/fieldseparator/
---
## FieldSeparator class


Representerar en Word-fältseparator som separerar fältkoden från fältresultatet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSeparator : public Aspose::Words::Fields::FieldChar
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Returnerar fältets typ. |
| [get_Font](../../aspose.words/inline/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Hämtar eller anger om föräldrafältet är låst (bör inte beräkna om sitt resultat). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [FieldSeparator](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Hämtar föräldern [Paragraph](../../aspose.words/paragraph/) till denna nod. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Returnerar ett fält för fälttecknet. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Hämtar det speciella tecknet som denna nod representerar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


[FieldSeparator](./) is an inline-level node and represented by the [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

Ett komplett fält i ett Microsoft Word-dokument är en komplex struktur som består av ett fältstarttecken, fältkod, fältseparator‑tecken, fältresultat och fältslut‑tecken. Vissa fält har bara fältstart, fältkod och fältslut.

För att enkelt infoga ett nytt fält i ett dokument, använd metoden [InsertField()](../).
## Se även

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
