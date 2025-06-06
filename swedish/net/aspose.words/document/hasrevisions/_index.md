---
title: Document.HasRevisions
linktitle: HasRevisions
articleTitle: HasRevisions
second_title: Aspose.Words för .NET
description: Ta reda på om ditt dokument har spårade ändringar med egenskapen HasRevisions. Hantera enkelt redigeringar och effektivisera ditt arbetsflöde.
type: docs
weight: 210
url: /sv/net/aspose.words/document/hasrevisions/
---
## Document.HasRevisions property

Returer`sann` om dokumentet har några spårade ändringar.

```csharp
public bool HasRevisions { get; }
```

## Anmärkningar

Den här egenskapen är en genväg för att jämföra[`Count`](../../revisioncollection/count/) till noll.

## Exempel

Visar hur man arbetar med revisioner i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal redigering av dokumentet räknas inte som en revision.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// För att registrera våra redigeringar som revisioner måste vi ange en författare och sedan börja spåra dem.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Denna flagga motsvarar alternativet "Granska" -> "Spårning" -> "Spåra ändringar" i Microsoft Word.
// Metoden "StartTrackRevisions" påverkar inte dess värde,
// och dokumentet spårar revisioner programmatiskt trots att det har värdet "false".
// Om vi öppnar det här dokumentet med Microsoft Word kommer det inte att spåra revisioner.
Assert.IsFalse(doc.TrackRevisions);

// Vi har lagt till text med hjälp av dokumentbyggaren, så den första revisionen är en revision av infogningstyp.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Ta bort en körning för att skapa en revision av borttagningstyp.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Om du lägger till en ny revision placeras den i början av revisionssamlingen.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Infoga revisioner visas i dokumentets brödtext redan innan vi accepterar/avvisar revisionen.
// Om du avvisar revisionen tas dess noder bort från brödtexten. Omvänt tas noder som utgör revisionerna bort.
// dröjer sig också kvar i dokumentet tills vi accepterar revisionen.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Om du accepterar borttagningsrevisionen tas dess överordnade nod bort från styckets text.
// och sedan ta bort själva samlingens revision.
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

// Den flyttande revisionen är nu på index 1. Avvisa revisionen för att kassera dess innehåll.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
