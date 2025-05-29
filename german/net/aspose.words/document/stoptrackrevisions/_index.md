---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie mit der Methode „StopTrackRevisions“ automatische Markierungen von Dokumentänderungen verhindern und so Ihre Bearbeitungseffizienz und Dokumentübersichtlichkeit verbessern.
type: docs
weight: 770
url: /de/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Stoppt die automatische Kennzeichnung von Dokumentänderungen als Revisionen.

```csharp
public void StopTrackRevisions()
```

## Beispiele

Zeigt, wie Sie beim Bearbeiten eines Dokuments Revisionen nachverfolgen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Bearbeiten eines Dokuments zählt normalerweise nicht als Revision, bis wir mit der Nachverfolgung beginnen.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Beenden Sie die Revisionsverfolgung, um zukünftige Bearbeitungen nicht als Revisionen zu zählen.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Durch das Erstellen von Revisionen werden Datum und Uhrzeit des Vorgangs angegeben.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir mit der Verfolgung von Revisionen beginnen.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Wir können diese Revisionen programmgesteuert akzeptieren/ablehnen
// durch Aufrufen von Methoden wie Document.AcceptAllRevisions oder der Accept-Methode jeder Revision.
// In Microsoft Word können wir diese über „Überprüfen“ -> „Änderungen“ manuell bearbeiten.
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Siehe auch

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
