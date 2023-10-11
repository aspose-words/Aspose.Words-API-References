---
title: Class Body
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Body klass. Representerar en behållare för huvudtexten i ett avsnitt.
type: docs
weight: 30
url: /sv/net/aspose.words/body/
---
## Body class

Representerar en behållare för huvudtexten i ett avsnitt.

För att lära dig mer, besök[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class Body : Story
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Body](body/)(DocumentBase) | Initierar en ny instans av`Body` class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Får första stycket i berättelsen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | ReturnerarBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Får en samling stycken som är omedelbara barn till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Hämtar den överordnade delen av denna berättelse. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Hämtar typen av denna berättelse. |
| [Tables](../../aspose.words/story/tables/) { get; } | Får en samling tabeller som är omedelbara barn till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(DocumentVisitor) | Accepterar en besökare. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | En genvägsmetod som skapar en[`Paragraph`](../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Tar bort alla former från texten i denna berättelse. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Om det sista underordnade inte är ett stycke, skapar och lägger till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

`Body` kan innehålla[`Paragraph`](../paragraph/) och[`Tabell`](../../aspose.words.tables/table/) barnnoder.

`Body` är en nod på sektionsnivå och kan bara vara ett barn till[`Section`](../section/) . Det kan bara finnas en`Body` i en[`Section`](../section/).

En minimal giltig`Body` måste innehålla minst en[`Paragraph`](../paragraph/).

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

* class [Story](../story/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


