---
title: Class Inline
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Inline klass. Basklass för noder på inlinenivå som kan ha teckenformatering associerad med dem men som inte kan ha egna underordnade noder.
type: docs
weight: 3060
url: /sv/net/aspose.words/inline/
---
## Inline class

Basklass för noder på inline-nivå som kan ha teckenformatering associerad med dem, men som inte kan ha egna underordnade noder.

```csharp
public abstract class Inline : Node
```

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
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Hämtar typen av denna nod. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

En klass som härrör från **I kö** kan vara ett barn till **Paragraf**.

### Exempel

Visar hur man bestämmer revisionstypen för en inline-nod.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// När vi redigerar dokumentet medan alternativet "Spåra ändringar", som finns i via Granska -> Spårning,
// är aktiverat i Microsoft Word, de ändringar vi tillämpar räknas som revisioner.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revisioner med
// anropar dokumentets "StartTrackRevisions"-metod och stoppar spårningen genom att använda "StopTrackRevisions"-metoden.
// Vi kan antingen acceptera revisioner för att assimilera dem i dokumentet
// eller avvisa dem för att effektivt ändra den föreslagna ändringen.
Assert.AreEqual(6, doc.Revisions.Count);

// Föräldernoden för en revision är den körning som revisionen avser. En Run är en Inline-nod.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Nedan finns fem typer av revisioner som kan flagga en Inline-nod.
// 1 - En "infoga" revision:
// Denna revidering sker när vi infogar text medan vi spårar ändringar.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - En "format"-revision:
// Denna revidering sker när vi ändrar formateringen av text medan vi spårar ändringar.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - En "flytta från" revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// medan du spårar ändringar visas två versioner.
// Revisionen "flytta från" är en kopia av texten som ursprungligen var innan vi flyttade den.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - En "flytta till" revision:
// "Flytta till"-revisionen är texten som vi flyttade i sin nya position i dokumentet.
// "Flytta från" och "flytta till" revisioner visas i par för varje flytt revision vi utför.
// Att acceptera en flyttversion raderar "flytta från"-revisionen och dess text,
// och behåller texten från "flytta till"-revisionen.
// Att avvisa en flyttversion behåller omvänt "flytta från"-revisionen och tar bort "flytta till"-revisionen.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - En "radera" revision:
// Denna revidering sker när vi tar bort text medan vi spårar ändringar. När vi tar bort text som denna,
// det kommer att stanna i dokumentet som en revision tills vi antingen accepterar revisionen,
// som kommer att ta bort texten för gott, eller förkasta revisionen, vilket kommer att behålla texten vi raderade där den var.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Se även

* class [Node](../node/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


