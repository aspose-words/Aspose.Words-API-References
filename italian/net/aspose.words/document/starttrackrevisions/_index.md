---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words per .NET
description: Traccia senza sforzo le modifiche ai documenti con il metodo StartTrackRevisions. Contrassegna automaticamente tutte le modifiche come revisioni per una collaborazione fluida e chiara.
type: docs
weight: 760
url: /it/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Inizia a contrassegnare automaticamente tutte le ulteriori modifiche apportate al documento a livello di programmazione come modifiche di revisione.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |

## Osservazioni

Se si richiama questo metodo e poi si apportano delle modifiche al documento a livello di programmazione, si salva il documento e in seguito lo si apre in MS Word; tali modifiche verranno visualizzate come revisioni.

Attualmente Aspose.Words supporta solo il tracciamento degli inserimenti e delle eliminazioni dei nodi. Le modifiche di formattazione non vengono registrate come revisioni.

Il tracciamento automatico delle modifiche è supportato sia quando si modifica questo documento tramite manipolazioni del nodo sia quando si utilizza[`DocumentBuilder`](../../documentbuilder/)

Questo metodo non modifica il[`TrackRevisions`](../trackrevisions/) opzione e non utilizza il suo valore ai fini del monitoraggio delle revisioni.

## Esempi

Mostra come tenere traccia delle revisioni durante la modifica di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Solitamente la modifica di un documento non viene considerata una revisione finché non iniziamo a monitorarla.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Interrompere il monitoraggio delle revisioni per non conteggiare più le modifiche future come revisioni.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// La creazione delle revisioni fornisce loro una data e un'ora dell'operazione.
// Possiamo disattivarlo passando DateTime.MinValue quando iniziamo a monitorare le revisioni.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Possiamo accettare/rifiutare queste revisioni a livello di programmazione
// chiamando metodi come Document.AcceptAllRevisions o il metodo Accept di ogni revisione.
// In Microsoft Word possiamo elaborarli manualmente tramite "Revisione" -> "Modifiche".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Guarda anche

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Inizia a contrassegnare automaticamente tutte le ulteriori modifiche apportate al documento a livello di programmazione come modifiche di revisione.

```csharp
public void StartTrackRevisions(string author)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |

## Osservazioni

Se si richiama questo metodo e poi si apportano delle modifiche al documento a livello di programmazione, si salva il documento e in seguito lo si apre in MS Word; tali modifiche verranno visualizzate come revisioni.

Attualmente Aspose.Words supporta solo il tracciamento degli inserimenti e delle eliminazioni dei nodi. Le modifiche di formattazione non vengono registrate come revisioni.

Il tracciamento automatico delle modifiche è supportato sia quando si modifica questo documento tramite manipolazioni del nodo sia quando si utilizza[`DocumentBuilder`](../../documentbuilder/)

Questo metodo non modifica il[`TrackRevisions`](../trackrevisions/) opzione e non utilizza il suo valore ai fini del monitoraggio delle revisioni.

## Esempi

Mostra come tenere traccia delle revisioni durante la modifica di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Solitamente la modifica di un documento non viene considerata una revisione finché non iniziamo a monitorarla.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Interrompere il monitoraggio delle revisioni per non conteggiare più le modifiche future come revisioni.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// La creazione delle revisioni fornisce loro una data e un'ora dell'operazione.
// Possiamo disattivarlo passando DateTime.MinValue quando iniziamo a monitorare le revisioni.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Possiamo accettare/rifiutare queste revisioni a livello di programmazione
// chiamando metodi come Document.AcceptAllRevisions o il metodo Accept di ogni revisione.
// In Microsoft Word possiamo elaborarli manualmente tramite "Revisione" -> "Modifiche".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Guarda anche

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
