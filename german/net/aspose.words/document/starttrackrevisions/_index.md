---
title: StartTrackRevisions
second_title: Aspose.Words für .NET-API-Referenz
description: Beginnt automatisch damit alle weiteren Änderungen die Sie programmgesteuert am Dokument vornehmen als Revisionsänderungen zu markieren.
type: docs
weight: 690
url: /de/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

Beginnt automatisch damit, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Initialen des Autors für Überarbeitungen. |
| dateTime | DateTime | Datum und Uhrzeit für Überarbeitungen. |

### Bemerkungen

Wenn Sie diese Methode aufrufen und dann programmgesteuert einige Änderungen am Dokument vornehmen, das Dokument speichern und später das Dokument in MS Word öffnen, sehen Sie diese Änderungen als Überarbeitungen.

Derzeit unterstützt Aspose.Words nur die Verfolgung von Knoteneinfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen aufgezeichnet.

Die automatische Nachverfolgung von Änderungen wird sowohl beim Ändern dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung unterstützt[`DocumentBuilder`](../../documentbuilder)

Diese Methode ändert nichts an der[`TrackRevisions`](../trackrevisions) Option und verwendet ihren Wert nicht für die Revisionsverfolgung.

### Beispiele

Zeigt, wie Revisionen beim Bearbeiten eines Dokuments nachverfolgt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Bearbeiten eines Dokuments zählt normalerweise nicht als Überarbeitung, bis wir damit beginnen, es zu verfolgen.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Beenden Sie die Nachverfolgung von Revisionen, um zukünftige Änderungen nicht als Revisionen zu zählen.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit der Operation.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir mit der Verfolgung von Revisionen beginnen.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Wir können diese Überarbeitungen programmgesteuert akzeptieren/ablehnen
// durch Aufrufen von Methoden wie Document.AcceptAllRevisions oder der Accept-Methode jeder Revision.
// In Microsoft Word können wir sie manuell über "Überprüfen" -> "Änderungen".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Siehe auch

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

Beginnt automatisch damit, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```csharp
public void StartTrackRevisions(string author)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Initialen des Autors für Überarbeitungen. |

### Bemerkungen

Wenn Sie diese Methode aufrufen und dann programmgesteuert einige Änderungen am Dokument vornehmen, das Dokument speichern und später das Dokument in MS Word öffnen, sehen Sie diese Änderungen als Überarbeitungen.

Derzeit unterstützt Aspose.Words nur die Verfolgung von Knoteneinfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen aufgezeichnet.

Die automatische Nachverfolgung von Änderungen wird sowohl beim Ändern dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung unterstützt[`DocumentBuilder`](../../documentbuilder)

Diese Methode ändert nichts an der[`TrackRevisions`](../trackrevisions) Option und verwendet ihren Wert nicht für die Revisionsverfolgung.

### Beispiele

Zeigt, wie Revisionen beim Bearbeiten eines Dokuments nachverfolgt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Bearbeiten eines Dokuments zählt normalerweise nicht als Überarbeitung, bis wir damit beginnen, es zu verfolgen.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Beenden Sie die Nachverfolgung von Revisionen, um zukünftige Änderungen nicht als Revisionen zu zählen.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit der Operation.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir mit der Verfolgung von Revisionen beginnen.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Wir können diese Überarbeitungen programmgesteuert akzeptieren/ablehnen
// durch Aufrufen von Methoden wie Document.AcceptAllRevisions oder der Accept-Methode jeder Revision.
// In Microsoft Word können wir sie manuell über "Überprüfen" -> "Änderungen".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Siehe auch

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
