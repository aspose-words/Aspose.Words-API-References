---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Paragraph för att enkelt hantera och formatera textstycken och förbättra dina dokumentbehandlingsmöjligheter.
type: docs
weight: 5120
url: /sv/net/aspose.words/paragraph/
---
## Paragraph class

Representerar ett textstycke.

För att lära dig mer, besök[Arbeta med stycken](https://docs.aspose.com/words/net/working-with-paragraphs/) dokumentationsartikel.

```csharp
public class Paragraph : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Initierar en ny instans av`Paragraph` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Sant om denna styckebrytning är en stilseparator. En stilseparator gör att ett stycke kan bestå av delar som har olika styckestilar. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Ger åtkomst till egenskaperna för ramformatering. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Returnerar sant om det här objektet togs bort i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Sant om detta stycke är det sista stycket i en[`Cell`](../../aspose.words.tables/cell/) ; falskt annars. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Sant om detta stycke är det sista stycket i dokumentets sista avsnitt. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Sant om detta stycke är det sista stycket i[`HeaderFooter`](../headerfooter/) (huvudtextberättelse) av en[`Section`](../section/) ; falskt annars. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Sant om detta stycke är det sista stycket i[`Body`](../body/) (huvudtextberättelse) av en[`Section`](../section/) ; falskt annars. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Returnerar sant om objektets formatering ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Sant om detta stycke är ett direkt underordnat stycke till[`Cell`](../../aspose.words.tables/cell/) ; falskt annars. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Sant när stycket är ett objekt i en punktlista eller numrerad lista i den ursprungliga versionen. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Returer`sann` om det här objektet flyttades (raderades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Ger åtkomst till listformateringsegenskaperna för stycket. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Får en[`ListLabel`](./listlabel/)objekt som ger åtkomst till listnumreringsvärde och formatering för detta stycke. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | ReturerParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Ger åtkomst till teckensnittsformateringen för styckebrytningstecknet. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Ger åtkomst till styckeformateringsegenskaperna. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Hämtar föräldern[`Section`](../section/) av stycket. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Hämtar den överordnade artikeln på sektionsnivå som kan vara[`Body`](../body/) eller[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Ger åtkomst till den maskinskrivna samlingen av textbitar inuti stycket. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka slutet av dokumentets stycke. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka början av dokumentets stycke. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Lägger till ett fält i detta stycke. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Lägger till ett fält i detta stycke. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Lägger till ett fält i detta stycke. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Returnerar en matris med alla tabbstopp som tillämpats på detta stycke, inklusive indirekt tillämpade av format eller listor. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Hämtar texten i detta stycke inklusive slutet av stycket. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Infogar ett fält i detta stycke. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Infogar ett fält i detta stycke. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Infogar ett fält i detta stycke. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Kopplar samman körningar med samma formatering i stycket. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

`Paragraph` är en blocknivånod och kan vara ett barn till klasser härledda från [`Story`](../story/) eller[`InlineStory`](../inlinestory/).

`Paragraph` kan innehålla valfritt antal noder och bokmärken på inline-nivå.

Den kompletta listan över underordnade noder som kan förekomma inuti ett stycke består av [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Ett giltigt stycke i Microsoft Word avslutas alltid med ett styckebrytningstecken och ett minimalt giltigt stycke består bara av en styckebrytning.`Paragraph` Klassen lägger automatiskt till lämpligt styckebrytningstecken i slutet av och detta tecken är inte en del av undernoderna till`Paragraph` , därför a`Paragraph` kan vara tom.

Inkludera inte slutet av stycket[`ParagraphBreak`](../controlchar/paragraphbreak/) eller slutet av cellen[`Cell`](../controlchar/cell/) tecken inuti texten i stycket eftersom det kan göra stycket ogiltigt när dokumentet öppnas i Microsoft Word.

## Exempel

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan barn.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta undernoder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla i dess nodsamling igen.
// Skapa först en ny sektion och lägg sedan till den som ett underordnat avsnitt till rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ange vissa sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en brödtext, som innehåller och visar allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en körning,
// ange dess utseende och innehåll och lägg sedan till det som ett underordnat stycke.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Se även

* class [CompositeNode](../compositenode/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
