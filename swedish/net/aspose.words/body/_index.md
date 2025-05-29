---
title: Body Class
linktitle: Body
articleTitle: Body
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Body, ditt viktiga verktyg för att enkelt hantera avsnittstext och förbättra effektiviteten i dokumenthanteringen.
type: docs
weight: 220
url: /sv/net/aspose.words/body/
---
## Body class

Representerar en behållare för huvudtexten i ett avsnitt.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class Body : Story
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Body](body/)(*[DocumentBase](../documentbase/)*) | Initierar en ny instans av`Body` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Hämtar det första stycket i berättelsen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | ReturerBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Hämtar en samling stycken som är direkta underordnade stycken till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Hämtar huvudavsnittet för den här artikeln. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Hämtar typen av den här berättelsen. |
| [Tables](../../aspose.words/story/tables/) { get; } | Hämtar en samling tabeller som är direkta underordnade tabeller till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka slutet av dokumentets brödtext. |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka början av dokumentets brödtext. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | En genvägsmetod som skapar en[`Paragraph`](../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Tar bort alla former från texten i den här berättelsen. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Om det sista underordnade stycket inte är ett stycke skapas och läggs till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
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

`Body` kan innehålla[`Paragraph`](../paragraph/) och[`Tabell`](../../aspose.words.tables/table/) underordnade noder.

`Body` är en nod på sektionsnivå och kan bara vara underordnad[`Section`](../section/) . Det kan bara finnas en`Body` i en[`Section`](../section/).

En minimal giltig`Body` behöver innehålla minst en[`Paragraph`](../paragraph/).

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

* class [Story](../story/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
