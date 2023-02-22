---
title: Class Run
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Run klass. Representerar en serie tecken med samma teckensnittsformatering.
type: docs
weight: 4560
url: /sv/net/aspose.words/run/
---
## Run class

Representerar en serie tecken med samma teckensnittsformatering.

```csharp
public class Run : Inline
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Run](run/#constructor)(DocumentBase) | Initierar en ny instans av **Springa** class. |
| [Run](run/#constructor_1)(DocumentBase, string) | Initierar en ny instans av **Springa** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Font](../../aspose.words/inline/font/) { get; } | Ger tillgång till teckensnittsformateringen för detta objekt. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returnerar sant om denna nod kan innehålla andra noder. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returnerar **Sann** om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returnerar **Sann** om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/run/nodetype/) { get; } | Returnerar **NodeType.Run** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [Text](../../aspose.words/run/text/) { get; set; } | Hämtar eller ställer in texten för körningen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/run/accept/)(DocumentVisitor) | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| override [GetText](../../aspose.words/run/gettext/)() | Hämtar texten för körningen. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

All text i dokumentet lagras i rader av text.

**Springa** kan bara vara ett barn av **Paragraf** eller inline **StructuredDocumentTag**.

### Exempel

Visar hur man formaterar en serie text med dess teckensnittsegenskap.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

Visar hur man lägger till, uppdaterar och tar bort underordnade noder i en CompositeNodes samling av barn.

```csharp
Document doc = new Document();

// Ett tomt dokument har som standard ett stycke.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Sammansatta noder som vårt stycke kan innehålla andra sammansatta och infogade noder som underordnade.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Skapa ytterligare tre körnoder.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Dokumentets brödtext kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, som vi gjorde med den första körningen.
// Vi kan bestämma var textinnehållet i noder som vi infogar
// visas i dokumentet genom att ange en infogningsplats i förhållande till en annan nod i stycket.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Infoga den andra körningen i stycket framför den första körningen.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Infoga den tredje körningen efter den första körningen.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Infoga den första körningen till början av styckets samling av underordnade noder.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga underordnade noder.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Se även

* class [Inline](../inline/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


