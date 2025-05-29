---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder MoveTo-metoden för att enkelt navigera bland inbäddade noder och effektivt placera markören i styckeslut för smidig dokumentredigering.
type: docs
weight: 520
url: /sv/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Flyttar markören till en inbäddad nod eller till slutet av ett stycke.

```csharp
public void MoveTo(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden måste vara ett stycke eller ett direkt underordnat stycke. |

## Anmärkningar

Närnod är en nod på inline-nivå, flyttas markören till denna nod och ytterligare innehåll infogas före den noden.

Närnod är en[`Paragraph`](../../paragraph/)markören flyttas till slutet av paragraph och ytterligare innehåll infogas precis före styckebrytningen.

Närnod är en blocknivånod men inte en[`Paragraph`](../../paragraph/), markören flyttas till slutet av det första stycket i blocknivånoden och ytterligare innehåll infogas precis före styckebrytningen.

## Exempel

Visar hur man flyttar markörpositionen för en DocumentBuilder till en specifik nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Dokumentbyggaren har en markör som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Den här markören fungerar på samma sätt som den blinkande markören i Microsoft Word,
// och den hamnar också alltid direkt efter en nod som byggaren just infogat.
// För att lägga till innehåll i en annan del av dokumentet,
// vi kan flytta markören till en annan nod med metoden "Flytta till".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Markören är nu framför noden som vi flyttade den till.
// Om du lägger till en andra körning infogas den framför den första körningen.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Visar hur man flyttar markören i ett dokumentbyggare till olika noder i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett giltigt bokmärke, en entitet som består av noder omgivna av en bokmärkesstartnod,
 // och en bokmärkesslutnod.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Dokumentbyggarens markör är alltid före den nod som vi senast lade till med den.
// Om byggarens markör är i slutet av dokumentet, kommer dess nuvarande nod att vara null.
// Den föregående noden är bokmärkets slutnod som vi senast lade till.
// Om du lägger till nya noder med byggaren läggs de till i den sista noden.
Assert.Null(builder.CurrentNode);

// Om vi vill redigera en annan del av dokumentet med verktyget,
// vi måste flytta markören till noden vi vill redigera.
builder.MoveToBookmark("MyBookmark");

// Att flytta den till ett bokmärke flyttar den till den första noden inom bokmärkets start- och slutnoder, den bifogade körningen.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Vi kan också flytta markören till en enskild nod så här.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Vi kan använda specifika metoder för att gå till början/slutet av ett dokument.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Se även

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
