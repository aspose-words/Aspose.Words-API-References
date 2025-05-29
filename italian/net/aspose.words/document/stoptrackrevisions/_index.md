---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo StopTrackRevisions per impedire la marcatura automatica delle modifiche ai documenti, migliorando l'efficienza delle modifiche e la chiarezza dei documenti.
type: docs
weight: 770
url: /it/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Interrompe la marcatura automatica delle modifiche al documento come revisioni.

```csharp
public void StopTrackRevisions()
```

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

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
