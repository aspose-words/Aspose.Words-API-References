---
title: "Aspose::Words::HeaderFooter klass"
linktitle: "HeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::HeaderFooter klass. Representerar en behållare för rubrik- eller fottexten i ett avsnitt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words/headerfooter/
---
## HeaderFooter class


Representerar en behållare för rubrik- eller sidfotstexten i en sektion. För att läsa mer, besök artikeln [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/) i dokumentationen.

```cpp
class HeaderFooter : public Aspose::Words::Story
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av rubriken. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av rubriken. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](../story/appendparagraph/)(const System::String\&) | En genvägsmetod som skapar ett [Paragraph](../paragraph/)‑objekt med valfri text och lägger till det i slutet av detta objekt. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [DeleteShapes](../story/deleteshapes/)() | Raderar alla former från texten i den här berättelsen. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstParagraph](../story/get_firstparagraph/)() override | Hämtar det första stycket i berättelsen. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_HeaderFooterType](./get_headerfootertype/)() | Hämtar typen av denna rubrik/fot. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsHeader](./get_isheader/)() | Sant om detta [HeaderFooter](./)-objekt är en rubrik. |
| [get_IsLinkedToPrevious](./get_islinkedtoprevious/)() | Sant om denna rubrik eller fot är länkad till motsvarande rubrik eller fot i föregående avsnitt. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastParagraph](../story/get_lastparagraph/)() override | Hämtar det sista stycket i berättelsen. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [HeaderFooter](../nodetype/). |
| [get_Paragraphs](../story/get_paragraphs/)() override | Hämtar en samling stycken som är omedelbara barn till berättelsen. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentSection](./get_parentsection/)() | Hämtar föräldraavsnittet för detta story. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_StoryType](../story/get_storytype/)() override | Hämtar typen av den här storyn. |
| [get_Tables](../story/get_tables/)() override | Hämtar en samling tabeller som är omedelbara barn till storyn. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetText](../compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [HeaderFooter](./headerfooter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::HeaderFooterType) | Skapar ett nytt sidhuvud eller sidfot av den angivna typen. |
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
| [set_IsLinkedToPrevious](./set_islinkedtoprevious/)(bool) | Inställare för [Aspose::Words::HeaderFooter::get_IsLinkedToPrevious](./get_islinkedtoprevious/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/). There can only be one [HeaderFooter](./) of each [HeaderFooterType](./get_headerfootertype/) in a [Section](../section/).

Om [Section](../section/) inte har ett [HeaderFooter](./) av en specifik typ eller om [HeaderFooter](./) saknar barnnoder, anses detta sidhuvud/sidfötter vara länkat till sidhuvudet/sidfoten av samma typ i föregående avsnitt i Microsoft Word.

När [HeaderFooter](./) innehåller minst ett [Paragraph](../paragraph/), betraktas den inte längre som länkad till föregående i Microsoft Word.

## Exempel



Visar hur man skapar ett sidhuvud och en sidfot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett sidhuvud och lägg till ett stycke i det. Texten i det stycket
// kommer att visas högst upp på varje sida i detta avsnitt, ovanför huvudtexten.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Skapa en sidfot och lägg till ett stycke i den. Texten i det stycket
// kommer att visas längst ner på varje sida i detta avsnitt, under huvudtexten.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


Visar hur man tar bort alla sidfötter från ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Iterera genom varje avsnitt och ta bort sidfötter av alla typer.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Det finns tre typer av sidfot- och sidhuvudtyper.
    // 1 -  Det \"Första\" sidhuvud/sidfoten, som endast visas på den första sidan i ett avsnitt.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  Det \"Primära\" sidhuvud/sidfoten, som visas på udda sidor.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  Det \"Jämna\" sidhuvud/sidfoten, som visas på jämna sidor.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Visar hur man ersätter text i ett dokuments sidfot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Se även

* Class [Story](../story/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
