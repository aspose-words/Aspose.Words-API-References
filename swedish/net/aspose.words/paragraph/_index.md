---
title: Paragraph
second_title: Aspose.Words för .NET API Referens
description: Representerar ett textstycke.
type: docs
weight: 4150
url: /sv/net/aspose.words/paragraph/
---
## Paragraph class

Representerar ett textstycke.

```csharp
public class Paragraph : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Initierar en ny instans av **Paragraf** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Sant om denna styckebrytning är en stilavskiljare. En stilavgränsare tillåter one stycke att bestå av delar som har olika styckestilar. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Ger tillgång till styckeformateringsegenskaperna. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Sant om detta stycke är det sista stycket i en[`Cell`](../../aspose.words.tables/cell/) ; falskt annars. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Sant om detta stycke är det sista stycket i den sista delen av dokumentet. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Sant om detta stycke är det sista stycket i **Sidhuvud** (huvudtextberättelse) av en **Sektion** ; falskt annars. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Sant om detta stycke är det sista stycket i **Kropp** (huvudtextberättelse) av en **Sektion** ; falskt annars. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Sant om det här stycket är ett omedelbart barn till[`Cell`](../../aspose.words.tables/cell/) ; falskt annars. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Sant när stycket är ett objekt i en punktlista eller numrerad lista i originalversionen. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Returnerar **Sann** om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Returnerar **Sann** om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Ger tillgång till listformateringsegenskaperna för stycket. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Får en[`ListLabel`](./listlabel/) objekt som ger tillgång till listnumreringsvärde och formatering för detta stycke. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | Returnerar **NodeType.Paragraph** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Ger tillgång till teckensnittsformateringen för styckebrytningstecknet. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Ger tillgång till styckeformateringsegenskaperna. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Hämtar föräldern[`Section`](../section/) i stycket. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Hämtar den överordnade berättelsen på sektionsnivå som kan vara[`Body`](../body/) eller[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Ger tillgång till den maskinskrivna samlingen av textbitar i stycket. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Lägger till ett fält i detta stycke. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Lägger till ett fält i detta stycke. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Lägger till ett fält i detta stycke. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserverad för systemanvändning. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Returnerar array av alla tabbstopp som tillämpas på detta stycke, inklusive applicerade indirekt av stilar eller listor. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Hämtar texten i detta stycke inklusive slutet av styckets tecken. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Infogar ett fält i detta stycke. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Infogar ett fält i detta stycke. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Infogar ett fält i detta stycke. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Joins körs med samma formatering i stycket. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

[`Paragraph`](./paragraph/) är en nod på blocknivå och kan vara ett barn av klasser härledda från [`Story`](../story/) eller[`InlineStory`](../inlinestory/).

[`Paragraph`](./paragraph/) kan innehålla valfritt antal noder och bokmärken på inline-nivå.

Den fullständiga listan över underordnade noder som kan förekomma i ett stycke består av [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Ett giltigt stycke i Microsoft Word slutar alltid med ett styckebrytningstecken och ett minimalt giltigt stycke består bara av en styckebrytning. De **Paragraf** Klassen lägger automatiskt till lämpligt styckebrytningstecken i slutet och detta tecken är inte en del av undernoderna i **Paragraf** , därför a **Paragraf** kan vara tom.

Inkludera inte slutet av stycket[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak/) eller slutet av cellen[`ControlChar.Cell`](../controlchar/cell/) tecken i texten i stycket eftersom det kan göra stycket ogiltigt när dokumentet öppnas i Microsoft Word.

### Exempel

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan underordnade.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta underordnade noder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla på dess nodsamling.
// Skapa först ett nytt avsnitt och lägg sedan till det som ett underordnat dokument i rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ställ in några sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en kropp som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en löprunda,
// ställ in dess utseende och innehåll och lägg sedan till det som ett barn till stycket.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
