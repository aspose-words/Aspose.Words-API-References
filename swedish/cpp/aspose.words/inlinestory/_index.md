---
title: "Aspose::Words::InlineStory class"
linktitle: "InlineStory"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::InlineStory class. Basisklass för inline-nivånoder som kan innehålla stycken och tabeller. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 37000
url: /sv/cpp/aspose.words/inlinestory/
---
## InlineStory class


Basklass för inline-noder som kan innehålla stycken och tabeller. För att lära dig mer, besök dokumentationsartikeln [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) i dokumentationen.

```cpp
class InlineStory : public Aspose::Words::CompositeNode,
                    public Aspose::Words::IInline,
                    public Aspose::Words::IStory
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepterar en besökare. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXEnd-metoden hos den angivna dokumentbesökaren. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXStart-metoden hos den angivna dokumentbesökaren. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [EnsureMinimum](./ensureminimum/)() | Om den sista underordnade inte är ett stycke, skapas och läggs ett tomt stycke till. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstParagraph](./get_firstparagraph/)() override | Hämtar det första stycket i berättelsen. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för ankarkaraktären i detta objekt. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastParagraph](./get_lastparagraph/)() override | Hämtar det sista stycket i berättelsen. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Hämtar typen av denna nod. |
| [get_Paragraphs](./get_paragraphs/)() override | Hämtar en samling stycken som är omedelbara barn till berättelsen. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](./get_parentparagraph/)() | Hämtar föräldern [Paragraph](../paragraph/) till denna nod. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| virtual [get_StoryType](./get_storytype/)() | Returnerar typen av berättelsen. |
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


[InlineStory](./) is a container for block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

Klasserna som ärver från [InlineStory](./) är inline-nivånoder som kan innehålla sin egen text (paragrafer och tabeller). Till exempel innehåller en [Comment](../comment/) nod texten för en kommentar och en [Footnote](../../aspose.words.notes/footnote/) innehåller texten för en fotnot.

## Exempel



Visar hur man infogar och anpassar fotnoter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till text och referera den med en fotnot. Denna fotnot kommer att placera en liten upphöjd referens
// markör efter den text den refererar till och skapa ett post under huvudtexten längst ner på sidan.
// Denna post kommer att innehålla fotnotens referensmarkör och referenstexten,
// vilken vi kommer att skicka till dokumentbyggarens "InsertFootnote"-metod.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Om den här egenskapen är satt till "true", blir vår fotnotens referensmärke
// kommer att vara dess index bland alla sektionens fotnoter.
// Detta är den första fotnoten, så referensmärket blir "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Vi kan flytta dokumentbyggaren in i fotnoten för att redigera dess referenstext.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Vi kan ange ett anpassat referensmärke som fotnoten kommer att använda istället för sitt indexnummer.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Ett bokmärke med flaggan "IsAuto" satt till true kommer fortfarande att visa sitt riktiga index
// även om tidigare bokmärken visar anpassade referensmärken, så blir detta bokmärkes referensmärke ett "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```


Visar hur man lägger till en kommentar i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// I Microsoft Word kan vi högerklicka på den här kommentaren i dokumentkroppen för att redigera den, eller svara på den.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Se även

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
