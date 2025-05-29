---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words för .NET
description: Navigera enkelt i dina dokument med DocumentBuilder MoveToBookmark-metoden, som direkt placerar markören vid valfritt bokmärke för förbättrad redigering.
type: docs
weight: 530
url: /sv/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Flyttar markören till ett bokmärke.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Namnet på bokmärket som markören ska flyttas till. |

### Returvärde

`sann` om bokmärket hittades;`falsk` annat.

## Anmärkningar

Flyttar markören till en position precis efter början av bokmärket med det angivna namnet .

Jämförelsen är inte skiftlägeskänslig. Om bokmärket inte hittades,`falsk` is returneras och markören flyttas inte.

Att infoga ny text ersätter inte befintlig text i bokmärket.

Observera att vissa bokmärken i dokumentet är tilldelade formulärfält. Om du flyttar till ett sådant bokmärke och infogar text där infogas texten i formulärfältets kod. Även om detta inte ogiltigförklarar formulärfältet kommer den infogade texten inte att synas eftersom den blir en del av fältkoden.

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

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Flyttar markören till ett bokmärke med större precision.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Namnet på bokmärket som markören ska flyttas till. |
| isStart | Boolean | När`sann` , flyttar markören till början av bokmärket. När`falsk`, flyttar markören till slutet av bokmärket. |
| isAfter | Boolean | När`sann` , flyttar markören så att den kommer efter start- eller slutpositionen för bookmark . När`falsk`flyttar markören så att den är före start- eller slutpositionen för bookmark . |

### Returvärde

`sann` om bokmärket hittades;`falsk` annat.

## Anmärkningar

Flyttar markören till en position före eller efter bokmärkets början eller slut.

Om önskad position inte är på inline-nivå, går man vidare till nästa stycke.

Jämförelsen är inte skiftlägeskänslig. Om bokmärket inte hittades,`falsk` is returneras och markören flyttas inte.

## Exempel

Visar hur man flyttar en dokumentbyggares nodinsättningspunktsmarkör till ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett giltigt bokmärke består av en BookmarkStart-nod, en BookmarkEnd-nod med en
// matchande bokmärkesnamn någonstans efteråt, och innehåll omgivet av dessa noder.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Det finns fyra sätt att flytta markören i en dokumentbyggare till ett bokmärke.
// Om vi är mellan noderna BookmarkStart och BookmarkEnd, kommer markören att vara inuti bokmärket.
// Det här betyder att all text som läggs till av skaparen kommer att bli en del av bokmärket.
// 1 - Utanför bokmärket, framför noden BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Inuti bokmärket, precis efter noden BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - Inuti bokmärket, precis framför BookmarkEnd-noden:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Utanför bokmärket, efter noden BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
