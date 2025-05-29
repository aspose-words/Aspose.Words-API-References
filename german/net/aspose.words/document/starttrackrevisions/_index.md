---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words für .NET
description: Verfolgen Sie Dokumentänderungen mühelos mit der Methode „StartTrackRevisions“. Markieren Sie alle Änderungen automatisch als Revisionen für eine reibungslose Zusammenarbeit und mehr Übersichtlichkeit.
type: docs
weight: 760
url: /de/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |

## Bemerkungen

Wenn Sie diese Methode aufrufen und dann programmgesteuert einige Änderungen am Dokument vornehmen, das Dokument speichern und später in MS Word öffnen, werden Ihnen diese Änderungen als Revisionen angezeigt.

Derzeit unterstützt Aspose.Words nur die Verfolgung von Knoteneinfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen aufgezeichnet.

Die automatische Nachverfolgung von Änderungen wird sowohl bei der Änderung dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung von[`DocumentBuilder`](../../documentbuilder/)

Diese Methode ändert nichts an der[`TrackRevisions`](../trackrevisions/) Option und verwendet ihren Wert nicht zum Zwecke der Revisionsverfolgung.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```csharp
public void StartTrackRevisions(string author)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |

## Bemerkungen

Wenn Sie diese Methode aufrufen und dann programmgesteuert einige Änderungen am Dokument vornehmen, das Dokument speichern und später in MS Word öffnen, werden Ihnen diese Änderungen als Revisionen angezeigt.

Derzeit unterstützt Aspose.Words nur die Verfolgung von Knoteneinfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen aufgezeichnet.

Die automatische Nachverfolgung von Änderungen wird sowohl bei der Änderung dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung von[`DocumentBuilder`](../../documentbuilder/)

Diese Methode ändert nichts an der[`TrackRevisions`](../trackrevisions/) Option und verwendet ihren Wert nicht zum Zwecke der Revisionsverfolgung.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
