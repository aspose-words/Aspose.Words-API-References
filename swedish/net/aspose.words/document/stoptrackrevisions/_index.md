---
title: Document.StopTrackRevisions
second_title: Aspose.Words för .NET API Referens
description: Document metod. Stoppar automatisk markering av dokumentändringar som revisioner.
type: docs
weight: 740
url: /sv/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Stoppar automatisk markering av dokumentändringar som revisioner.

```csharp
public void StopTrackRevisions()
```

### Exempel

Visar hur man spårar revisioner medan man redigerar ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Att redigera ett dokument räknas vanligtvis inte som en revision förrän vi börjar spåra dem.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Sluta spåra revisioner för att inte räkna några framtida redigeringar som revisioner.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Att skapa revisioner ger dem ett datum och tid för operationen.
// Vi kan inaktivera detta genom att skicka DateTime.MinValue när vi börjar spåra revisioner.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Vi kan acceptera/förkasta dessa ändringar programmatiskt
// genom att anropa metoder som Document.AcceptAllRevisions, eller varje versions Accept-metod.
// I Microsoft Word kan vi bearbeta dem manuellt via "Review" -> "Ändringar".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Se även

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


