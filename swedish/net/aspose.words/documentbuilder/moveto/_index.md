---
title: DocumentBuilder.MoveTo
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Flyttar markören till en inlinenod eller till slutet av ett stycke.
type: docs
weight: 460
url: /sv/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Flyttar markören till en inline-nod eller till slutet av ett stycke.

```csharp
public void MoveTo(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden måste vara ett stycke eller ett direkt underordnat stycke. |

### Anmärkningar

Närnod är en nod på inline-nivå, flyttas markören till denna node och ytterligare innehåll kommer att infogas före den noden.

Närnod är en **Paragraf**, flyttas markören till slutet av stycket och ytterligare innehåll kommer att infogas strax före styckebrytningen.

Närnodär en nod på blocknivå men inte ett stycke, flyttas markören till slutet av första stycket till nod på blocknivå och ytterligare innehåll kommer att infogas strax före styckebrytningen.

### Exempel

Visar hur man flyttar en DocumentBuilders markörposition till en angiven nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Dokumentbyggaren har en markör, som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Den här markören fungerar på samma sätt som Microsoft Words blinkande markör,
// och det hamnar också alltid omedelbart efter någon nod som byggaren precis infogat.
// För att lägga till innehåll till en annan del av dokumentet,
// vi kan flytta markören till en annan nod med "MoveTo"-metoden.
// Markören är nu framför noden som vi flyttade den till.
// Om du lägger till en andra körning infogas den framför den första körningen.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text till slutet som tidigare.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Visar hur man flyttar en dokumentbyggares markör till olika noder i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett giltigt bokmärke, en enhet som består av noder som omges av en bokmärkesstartnod,
  // och en bokmärkesslutnod.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Dokumentbyggarens markör är alltid före den nod som vi senast lade till med den.
// Om byggarens markör är i slutet av dokumentet kommer dess nuvarande nod att vara null.
// Den föregående noden är bokmärkets slutnod som vi senast lade till.
// Lägga till nya noder med byggaren kommer att lägga till dem till den sista noden.
Assert.Null(builder.CurrentNode);

// Om vi vill redigera en annan del av dokumentet med byggaren,
// vi måste föra dess markör till den nod vi vill redigera.
builder.MoveToBookmark("MyBookmark");

// Om du flyttar den till ett bokmärke flyttas den till den första noden inom bokmärkets start- och slutnod, den bifogade körningen.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Vi kan också flytta markören till en enskild nod så här.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Vi kan använda specifika metoder för att flytta till början/slutet av ett dokument.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Se även

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


