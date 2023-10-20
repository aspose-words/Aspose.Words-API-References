---
title: RunCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words för .NET
description: RunCollection ToArray metod. Kopierar alla körningar från samlingen till en ny array av körningar i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/runcollection/toarray/
---
## RunCollection.ToArray method

Kopierar alla körningar från samlingen till en ny array av körningar.

```csharp
public Run[] ToArray()
```

### Returvärde

En rad körningar.

## Exempel

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

* class [Run](../../run/)
* class [RunCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
