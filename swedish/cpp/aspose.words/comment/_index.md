---
title: "Aspose::Words::Comment klass"
linktitle: "Kommentar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment klass. Representerar en behållare för texten i en kommentar. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/comment/
---
## Comment class


Representerar en behållare för texten i en kommentar. För att läsa mer, besök dokumentationsartikeln [Arbeta med kommentarer](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av kommentaren. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av kommentaren. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Lägger till ett svar på denna kommentar. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initierar en ny instans av klassen [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Initierar en ny instans av klassen [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Om den sista underordnade inte är ett stycke, skapas och läggs ett tomt stycke till. |
| [get_Ancestor](./get_ancestor/)() | Returnerar det överordnade [Comment](./)-objektet. Returnerar **null** för kommentarer på toppnivå. |
| [get_Author](./get_author/)() const | Returnerar eller anger författarnamnet för en kommentar. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_DateTime](./get_datetime/)() const | Hämtar datum och tid då kommentaren skapades. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Hämtar UTC-datum och -tid då kommentaren skapades. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Done](./get_done/)() const | Hämtar eller anger flagga som indikerar att kommentaren har markerats som klar. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Hämtar det första stycket i berättelsen. |
| [get_Font](../inlinestory/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för ankarkaraktären i detta objekt. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_Id](./get_id/)() const | Hämtar eller anger kommentarsidentifieraren. |
| [get_Initial](./get_initial/)() const | Returnerar eller anger initialerna för användaren som är kopplad till en specifik kommentar. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Hämtar det sista stycket i berättelsen. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Hämtar en samling stycken som är omedelbara barn till berättelsen. |
| [get_ParentId](./get_parentid/)() const | Hämtar föräldrakommentars-ID. Ett värde på **%-1** betyder att kommentaren saknar förälder. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Hämtar föräldern [Paragraph](../paragraph/) till denna nod. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Replies](./get_replies/)() | Returnerar en samling av [Comment](./)-objekt som är omedelbara barn till den angivna kommentaren. |
| [get_StoryType](./get_storytype/)() override | Returnerar [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Hämtar en samling tabeller som är omedelbara barn till storyn. |
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
| [RemoveAllReplies](./removeallreplies/)() | Tar bort alla svar på denna kommentar. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Tar bort det angivna svaret på denna kommentar. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../../aspose.words.markup/smarttag/)‑nedärvda noder för den aktuella noden. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../node/) som matchar XPath‑uttrycket. |
| [set_Author](./set_author/)(const System::String\&) | Sättare för [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Hämtar datum och tid då kommentaren skapades. |
| [set_Done](./set_done/)(bool) | Sättare för [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Sättare för [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Sättare för [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Anger föräldrakommentars-ID. Ett värde på **%-1** betyder att kommentaren saknar förälder. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Detta är en bekvämlighetsmetod som möjliggör att enkelt ange texten för kommentaren. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


En kommentar är en annotation som är förankrad till ett textområde eller till en position i texten. En kommentar kan innehålla en godtycklig mängd blocknivåinnehåll.

Om ett [Comment](./)-objekt förekommer på egen hand, är kommentaren förankrad till positionen för [Comment](./)-objektet.

För att förankra en kommentar till ett textområde krävs tre objekt: [Comment](./), [CommentRangeStart](../commentrangestart/) och [CommentRangeEnd](../commentrangeend/). Alla tre objekten måste dela samma [Id](./get_id/)-värde.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Exempel



Visar hur man lägger till en kommentar i ett dokument och sedan svarar på den.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Placera kommentaren på en nod i dokumentets kropp.
// Denna kommentar kommer att visas på platsen för dess stycke,
// utanför sidans högermarginal och med en prickad linje som förbinder den med dess stycke.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Lägg till ett svar, som kommer att visas under dess föräldrakommentar.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Kommentarer och svar är båda Comment-noder.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Kommentarer som inte svarar på andra kommentarer är "top-level". De har inga förfäderskommentarer.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Svar har en förfäderskommentar på toppnivå.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
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

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
