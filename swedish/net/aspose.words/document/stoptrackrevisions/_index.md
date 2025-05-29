---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words för .NET
description: Lär dig hur du använder StopTrackRevisions-metoden för att förhindra automatiska dokumentändringsmarkeringar, vilket förbättrar din redigeringseffektivitet och dokumentets tydlighet.
type: docs
weight: 770
url: /sv/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Stoppar automatisk markering av dokumentändringar som revisioner.

```csharp
public void StopTrackRevisions()
```

## Exempel

Visar hur man spårar revisioner när man redigerar ett dokument.

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
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Sluta spåra revisioner för att inte räkna framtida redigeringar som revisioner.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Att skapa revisioner ger dem ett datum och en tid för operationen.
// Vi kan inaktivera detta genom att skicka DateTime.MinValue när vi börjar spåra revisioner.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Vi kan acceptera/avvisa dessa revisioner programmatiskt
// genom att anropa metoder som Document.AcceptAllRevisions, eller varje revisions Accept-metod.
// I Microsoft Word kan vi bearbeta dem manuellt via "Granska" -> "Ändringar".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Se även

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
