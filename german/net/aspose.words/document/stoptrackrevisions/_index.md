---
title: Document.StopTrackRevisions
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Stoppt die automatische Markierung von Dokumentänderungen als Revisionen.
type: docs
weight: 740
url: /de/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Stoppt die automatische Markierung von Dokumentänderungen als Revisionen.

```csharp
public void StopTrackRevisions()
```

### Beispiele

Zeigt, wie Sie Revisionen beim Bearbeiten eines Dokuments verfolgen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Bearbeiten eines Dokuments zählt normalerweise nicht als Überarbeitung, bis wir mit der Nachverfolgung beginnen.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Die Verfolgung von Revisionen stoppen, um zukünftige Änderungen nicht als Revisionen zu zählen.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit des Vorgangs.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir mit der Nachverfolgung von Revisionen beginnen.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Wir können diese Revisionen programmgesteuert akzeptieren/ablehnen
// durch Aufrufen von Methoden wie Document.AcceptAllRevisions oder der Accept-Methode jeder Revision.
// In Microsoft Word können wir sie manuell über „Überprüfen“ -> bearbeiten. "Änderungen".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Siehe auch

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


