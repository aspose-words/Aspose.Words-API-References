---
title: DocumentBuilder.IsAtStartOfParagraph
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Returnerar sant om markören är i början av det aktuella stycket ingen text före markören.
type: docs
weight: 110
url: /sv/net/aspose.words/documentbuilder/isatstartofparagraph/
---
## DocumentBuilder.IsAtStartOfParagraph property

Returnerar sant om markören är i början av det aktuella stycket (ingen text före markören).

```csharp
public bool IsAtStartOfParagraph { get; }
```

### Exempel

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

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


