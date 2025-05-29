---
title: InlineStory.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words för .NET
description: Upptäck InlineStorys IsInsertRevision-egenskap. Identifiera enkelt infogade objekt i Word med aktiverad ändringsspårning. Förbättra din dokumenthantering idag!
type: docs
weight: 40
url: /sv/net/aspose.words/inlinestory/isinsertrevision/
---
## InlineStory.IsInsertRevision property

Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsInsertRevision { get; }
```

## Exempel

Visar hur man visar revisionsrelaterade egenskaper för InlineStory-noder.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// När vi redigerar dokumentet medan alternativet "Spåra ändringar" är aktiverat, som finns via Granska -> Spårning,
// är aktiverat i Microsoft Word, räknas de ändringar vi tillämpar som revisioner.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revisioner genom att
// anropar dokumentets metod "StartTrackRevisions" och stoppar spårning med hjälp av metoden "StopTrackRevisions".
// Vi kan antingen acceptera ändringar för att integrera dem i dokumentet
// eller avvisa dem för att ångra och ignorera den föreslagna ändringen.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Nedan följer fem typer av revisioner som kan flagga en InlineStory-nod.
// 1 - En "infoga"-revision:
// Denna revision sker när vi infogar text medan vi spårar ändringar.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - En "flytt från"-revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// när ändringar spåras visas två revisioner.
// "Flytta från"-versionen är en kopia av texten ursprungligen innan vi flyttade den.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - En "flytta till"-revision:
// "Flytta till"-versionen är den text som vi flyttade till sin nya position i dokumentet.
// "Flytta från"- och "flytta till"-revisioner visas parvis för varje flyttrevision vi utför.
// Att acceptera en flyttversion raderar "flytta från"-versionen och dess text,
// och behåller texten från "flytta till"-revisionen.
// Att avvisa en flyttad revision behåller omvänt "flytta från" revisionen och tar bort "flytta till" revisionen.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - En "borttagnings"-revision:
// Denna revision sker när vi tar bort text medan vi spårar ändringar. När vi tar bort text som denna,
// den kommer att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
// vilket tar bort texten för gott, eller avvisar revisionen, vilket behåller texten vi raderade där den var.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Se även

* class [InlineStory](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
