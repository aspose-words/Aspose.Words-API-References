---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Section, din nyckel till att hantera enskilda dokumentavsnitt utan problem. Förbättra din dokumentredigeringsupplevelse idag!
type: docs
weight: 6560
url: /sv/net/aspose.words/section/
---
## Section class

Representerar ett enda avsnitt i ett dokument.

För att lära dig mer, besök[Arbeta med sektioner](https://docs.aspose.com/words/net/working-with-sections/) dokumentationsartikel.

```csharp
public sealed class Section : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Initierar en ny instans av Section-klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Returnerar[`Body`](../body/) underordnad nod för sektionen. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Ger åtkomst till sidhuvud- och sidfotsnoderna i avsnittet. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | ReturerSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Returnerar ett objekt som representerar sidinställningar och sektionsegenskaper. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Sant om avsnittet är skyddat för formulär. När ett avsnitt är skyddat för formulär kan användare endast markera och ändra text i formulärfält i Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Infogar en kopia av innehållet i källavsnittet i slutet av detta avsnitt. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Rensar sektionen. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters)() | Rensar sidhuvuden och sidfoten i det här avsnittet. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters_1)(*bool*) | Rensar sidhuvuden och sidfoten i det här avsnittet. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Skapar en kopia av detta avsnitt. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Tar bort alla former (ritobjekt) från sidhuvuden och sidfoten i detta avsnitt. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Säkerställer att sektionen har[`Body`](./body/) med en[`Paragraph`](../paragraph/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Infogar en kopia av innehållet i källavsnittet i början av detta avsnitt. |
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

`Section` kan ha en[`Body`](../body/) och maximalt en[`HeaderFooter`](../headerfooter/) av varje[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) och[`HeaderFooter`](../headerfooter/) nodes kan vara i valfri ordning inuti`Section`.

Ett minimalt giltigt avsnitt måste ha[`Body`](../body/) med en[`Paragraph`](../paragraph/).

Varje sektion har sin egen uppsättning egenskaper som anger sidstorlek, orientering, marginaler etc.

Du kan skapa en kopia av ett avsnitt med hjälp av[`Clone`](../node/clone/)Kopian kan infogas i samma eller ett annat dokument.

För att lägga till, infoga eller ta bort ett helt avsnitt inklusive avsnittsbrytning och avsnittsegenskaper, använd metoder från[`Sections`](../document/sections/) objekt.

För att kopiera och infoga endast innehållet i avsnittet exklusive avsnittsbrytning och avsnittsegenskaper, använd[`AppendContent`](./appendcontent/) och[`PrependContent`](./prependcontent/) metoder.

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
