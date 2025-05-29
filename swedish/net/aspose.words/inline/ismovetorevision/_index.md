---
title: Inline.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen IsMoveToRevision i Microsoft Word spårar objektrörelser. Säkerställ korrekt ändringsspårning för smidig dokumentredigering!
type: docs
weight: 60
url: /sv/net/aspose.words/inline/ismovetorevision/
---
## Inline.IsMoveToRevision property

Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsMoveToRevision { get; }
```

## Exempel

Visar hur man bestämmer revisionstypen för en inline-nod.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// När vi redigerar dokumentet medan alternativet "Spåra ändringar" är aktiverat, som finns via Granska -> Spårning,
// är aktiverat i Microsoft Word, räknas de ändringar vi tillämpar som revisioner.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revisioner genom att
// anropar dokumentets metod "StartTrackRevisions" och stoppar spårning med hjälp av metoden "StopTrackRevisions".
// Vi kan antingen acceptera ändringar för att integrera dem i dokumentet
// eller avvisa dem för att effektivt ändra den föreslagna ändringen.
Assert.AreEqual(6, doc.Revisions.Count);

// Den överordnade noden för en revision är den körning som revisionen avser. En körning är en inline-nod.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Nedan följer fem typer av revisioner som kan flagga en Inline-nod.
// 1 - En "infoga"-revision:
// Denna revision sker när vi infogar text medan vi spårar ändringar.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - En "format"-revision:
// Denna revision sker när vi ändrar formateringen av text medan vi spårar ändringar.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - En "flytt från"-revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// när ändringar spåras visas två revisioner.
// "Flytta från"-versionen är en kopia av texten ursprungligen innan vi flyttade den.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - En "flytta till"-revision:
// "Flytta till"-versionen är den text som vi flyttade till sin nya position i dokumentet.
// "Flytta från"- och "flytta till"-revisioner visas parvis för varje flyttrevision vi utför.
// Att acceptera en flyttversion raderar "flytta från"-versionen och dess text,
// och behåller texten från "flytta till"-revisionen.
// Att avvisa en flyttad revision behåller omvänt "flytta från" revisionen och tar bort "flytta till" revisionen.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - En "borttagnings"-revision:
// Denna revision sker när vi tar bort text medan vi spårar ändringar. När vi tar bort text som denna,
// den kommer att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
// vilket tar bort texten för gott, eller avvisar revisionen, vilket behåller texten vi raderade där den var.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Se även

* class [Inline](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
