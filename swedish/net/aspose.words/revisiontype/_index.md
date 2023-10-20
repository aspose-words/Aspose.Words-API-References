---
title: RevisionType Enum
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words för .NET
description: Aspose.Words.RevisionType uppräkning. Anger vilken typ av ändring som spåras inRevision  i C#.
type: docs
weight: 4800
url: /sv/net/aspose.words/revisiontype/
---
## RevisionType enumeration

Anger vilken typ av ändring som spåras in[`Revision`](../revision/) .

```csharp
public enum RevisionType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Insertion | `0` | Nytt innehåll infogades i dokumentet. |
| Deletion | `1` | Innehåll togs bort från dokumentet. |
| FormatChange | `2` | Ändring av formatering tillämpades på den överordnade noden. |
| StyleDefinitionChange | `3` | Ändring av formatering tillämpades på den överordnade stilen. |
| Moving | `4` | Innehållet flyttades i dokumentet. |

## Exempel

Visar hur man arbetar med revisioner i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal redigering av dokumentet räknas inte som en revision.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// För att registrera våra redigeringar som revisioner måste vi deklarera en författare och sedan börja spåra dem.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Denna flagga motsvarar "Recension" -> "Spårning" -> Alternativet "Spåra ändringar" i Microsoft Word.
// "StartTrackRevisions"-metoden påverkar inte dess värde,
// och dokumentet spårar revisioner programmatiskt trots att det har värdet "false".
// Om vi öppnar det här dokumentet med Microsoft Word kommer det inte att spåra revisioner.
Assert.IsFalse(doc.TrackRevisions);

// Vi har lagt till text med hjälp av dokumentbyggaren, så den första revisionen är en revision av insättningstyp.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Ta bort en körning för att skapa en version av raderingstyp.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Om du lägger till en ny version placeras den i början av revisionssamlingen.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Infoga revisioner dyker upp i dokumentet innan vi accepterar/avvisar revisionen.
// Att avvisa revisionen kommer att ta bort dess noder från kroppen. Omvänt tar noder som utgör bort revisioner
// ligger också kvar i dokumentet tills vi accepterar revisionen.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Om du accepterar borttagningsrevisionen tas dess överordnade nod bort från stycketexten
// och ta sedan bort själva samlingens revision.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Flytta nu noden för att skapa en rörlig revisionstyp.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// Den rörliga revisionen är nu på index 1. Avvisa revisionen för att kassera dess innehåll.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
