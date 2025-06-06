---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words för .NET
description: Spåra enkelt dokumentändringar med StartTrackRevisions-metoden. Markera automatiskt alla redigeringar som revisioner för smidigt samarbete och tydlighet.
type: docs
weight: 760
url: /sv/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |

## Anmärkningar

Om du anropar den här metoden och sedan gör några ändringar i dokumentet programmatiskt, sparar dokumentet och senare öppnar dokumentet i MS Word, kommer du att se dessa ändringar som revideringar.

För närvarande stöder Aspose.Words endast spårning av nodinsättningar och borttagningar. Formateringsändringar registreras inte som revisioner.

Automatisk spårning av ändringar stöds både när detta dokument ändras via nodmanipulationer och när man använder[`DocumentBuilder`](../../documentbuilder/)

Denna metod ändrar inte[`TrackRevisions`](../trackrevisions/) alternativet och använder inte dess värde för revisionsspårning.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar.

```csharp
public void StartTrackRevisions(string author)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| author | String | Författarens initialer att använda för revideringar. |

## Anmärkningar

Om du anropar den här metoden och sedan gör några ändringar i dokumentet programmatiskt, sparar dokumentet och senare öppnar dokumentet i MS Word, kommer du att se dessa ändringar som revideringar.

För närvarande stöder Aspose.Words endast spårning av nodinsättningar och borttagningar. Formateringsändringar registreras inte som revisioner.

Automatisk spårning av ändringar stöds både när detta dokument ändras via nodmanipulationer och när man använder[`DocumentBuilder`](../../documentbuilder/)

Denna metod ändrar inte[`TrackRevisions`](../trackrevisions/) alternativet och använder inte dess värde för revisionsspårning.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
