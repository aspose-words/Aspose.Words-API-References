---
title: Footnote
second_title: Aspose.Words för .NET API Referens
description: Representerar en behållare för text i en fotnot eller slutnot.
type: docs
weight: 4020
url: /sv/net/aspose.words.notes/footnote/
---
## Footnote class

Representerar en behållare för text i en fotnot eller slutnot.

```csharp
public class Footnote : InlineStory
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Footnote](footnote)(DocumentBase, FootnoteType) | Initierar en instans av **Fotnot** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [Count](../../aspose.words/compositenode/count) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Får första stycket i berättelsen. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Ger tillgång till teckensnittsformateringen av ankartecknet för detta objekt. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype) { get; } | Returnerar ett värde som anger om detta är en fotnot eller slutnot. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| [IsAuto](../../aspose.words.notes/footnote/isauto) { get; set; } | Innehåller ett värde som anger om detta är en automatiskt numrerad fotnot eller fotnot med användardefinierat anpassat referensmärke. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Returnerar **Sann** om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Returnerar **Sann** om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype) { get; } | Returnerar **NodeType.Fotnot** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Får en samling stycken som är omedelbara barn till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Hämtar föräldern[`Paragraph`](../../aspose.words/paragraph) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark) { get; set; } | Hämtar/ställer in anpassat referensmärke som ska användas för denna fotnot. Standardvärdet är **tom sträng** (Empty ), vilket betyder att automatiskt numrerade fotnoter används. |
| override [StoryType](../../aspose.words.notes/footnote/storytype) { get; } | Returnerar **StoryType.Fotnotes** eller **StoryType.Slutnotes** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Får en samling tabeller som är omedelbara barn till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept)(DocumentVisitor) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserverad för systemanvändning. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Om det sista underordnade inte är ett stycke, skapar och lägger till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag) underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

De **Fotnot** klass används för att representera både fotnoter och slutnoter i ett Word-dokument.

**Fotnot** är en nod på inline-nivå och kan bara vara ett barn till **Paragraf**.

**Fotnot** kan innehålla **Paragraf** och **Tabell** barnnoder.

### Exempel

Visar hur man infogar och anpassar fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text och referera till den med en fotnot. Denna fotnot kommer att placera en liten upphöjd referens
// markera efter texten som den refererar till och skapa en post under huvudtexten längst ner på sidan.
// Denna post kommer att innehålla fotnotens referensmärke och referenstexten,
// som vi kommer att skicka till dokumentbyggarens "InsertFootnote"-metod.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Om den här egenskapen är inställd på "true", är vår fotnots referensmärke
// kommer att vara dess index bland alla avsnittets fotnoter.
// Detta är den första fotnoten, så referensmärket blir "1".
Assert.True(footnote.IsAuto);

// Vi kan flytta dokumentbyggaren inuti fotnoten för att redigera dess referenstext. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Vi kan ställa in ett anpassat referensmärke som fotnoten kommer att använda istället för dess indexnummer.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ett bokmärke med flaggan "IsAuto" inställd på sant kommer fortfarande att visa sitt verkliga index
// även om tidigare bokmärken visar anpassade referensmärken, så kommer detta bokmärkes referensmärke att vara en "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Se även

* class [InlineStory](../../aspose.words/inlinestory)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
