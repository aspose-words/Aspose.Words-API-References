---
title: DocumentBuilder.MoveToDocumentEnd
linktitle: MoveToDocumentEnd
articleTitle: MoveToDocumentEnd
second_title: Aspose.Words för .NET
description: Navigera enkelt i dina dokument med DocumentBuilder MoveToDocumentEnd-metoden och placera markören längst ner för smidig redigering.
type: docs
weight: 550
url: /sv/net/aspose.words/documentbuilder/movetodocumentend/
---
## DocumentBuilder.MoveToDocumentEnd method

Flyttar markören till slutet av dokumentet.

```csharp
public void MoveToDocumentEnd()
```

## Exempel

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

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
