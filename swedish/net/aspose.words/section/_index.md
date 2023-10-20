---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words för .NET
description: Aspose.Words.Section klass. Representerar en enskild sektion i ett dokument i C#.
type: docs
weight: 5730
url: /sv/net/aspose.words/section/
---
## Section class

Representerar en enskild sektion i ett dokument.

För att lära dig mer, besök[Arbeta med sektioner](https://docs.aspose.com/words/net/working-with-sections/) dokumentationsartikel.

```csharp
public sealed class Section : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Initierar en ny instans av klassen Sektion. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Returnerar[`Body`](../body/) barnnod för sektionen. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Ger åtkomst till noder för sidhuvuden och sidfötter i avsnittet. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | ReturnerarSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Returnerar ett objekt som representerar sidinställningar och avsnittsegenskaper. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Sant om avsnittet är skyddat för formulär. När en sektion är skyddad för formulär kan användare välja och ändra text endast i formulärfält i Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/) objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Infogar en kopia av innehållet i källavsnittet i slutet av det här avsnittet. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Rensar avsnittet. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Rensar sidhuvuden och sidfötter i det här avsnittet. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Skapar en dubblett av detta avsnitt. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Tar bort alla former (ritobjekt) från sidhuvuden och sidfötter i det här avsnittet. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Säkerställer att avsnittet har[`Body`](./body/) med en[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Infogar en kopia av innehållet i källavsnittet i början av det här avsnittet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Tar bort den angivna underordnade noden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

## Anmärkningar

`Section` kan ha en[`Body`](../body/) och max en[`HeaderFooter`](../headerfooter/) av varje[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) och[`HeaderFooter`](../headerfooter/) nodes kan vara i valfri ordning inuti`Section`.

Ett minimalt giltigt avsnitt måste ha[`Body`](../body/) med en[`Paragraph`](../paragraph/).

Varje avsnitt har sin egen uppsättning egenskaper som anger sidstorlek, orientering, marginaler etc.

Du kan skapa en kopia av ett avsnitt med[`Clone`](../node/clone/). Kopian kan infogas i samma eller ett annat dokument.

För att lägga till, infoga eller ta bort ett helt avsnitt inklusive avsnittsbrytning och avsnittsegenskaper använd metoderna i[`Sections`](../document/sections/) objekt.

För att kopiera och infoga bara innehållet i avsnittet exklusive avsnittet break och avsnittsegenskaper använd[`AppendContent`](./appendcontent/) och[`PrependContent`](./prependcontent/) metoder.

## Exempel

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
