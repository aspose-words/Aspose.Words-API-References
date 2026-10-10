---
title: "Aspose::Words::Markup::SmartTag-klass"
linktitle: "SmartTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SmartTag-klass. Detta element specificerar närvaron av en smart tag runt en eller flera inline‑strukturer (körningar, bilder, fält, osv.) inom ett stycke. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.markup/smarttag/
---
## SmartTag class


Detta element specificerar förekomsten av en smart tag runt en eller flera inline‑strukturer (körningar, bilder, fält, osv.) inom ett stycke. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SmartTag : public Aspose::Words::CompositeNode,
                 public Aspose::Words::Markup::IMarkupNode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av [SmartTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av [SmartTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Element](./get_element/)() const | Anger namnet på smart‑taggen i dokumentet. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [SmartTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Properties](./get_properties/)() const | En samling av smart‑taggens egenskaper. |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Uri](./get_uri/)() const | Anger namnrymdens URI för smart‑taggen. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla [SmartTag](./) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../../aspose.words/node/) som matchar XPath‑uttrycket. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Element](./set_element/)(const System::String\&) | Sättare för [Aspose::Words::Markup::SmartTag::get_Element](./get_element/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Uri](./set_uri/)(const System::String\&) | Sättare för [Aspose::Words::Markup::SmartTag::get_Uri](./get_uri/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initierar en ny instans av [SmartTag](./)-klassen. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Smart‑taggar är en typ av anpassad XML‑markup. Smart‑taggar erbjuder en möjlighet att bädda in kunddefinierad semantik i dokumentet genom att kunna ange ett grundläggande namnrymd/namn för en körning eller en uppsättning körningar i ett dokument.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

Den kompletta listan över barnnoder som kan förekomma inom en smart tagg består av [BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [CommentRangeStart](../../aspose.words/commentrangestart/), [CommentRangeEnd](../../aspose.words/commentrangeend/), [SmartTag](./).
## Se även

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
