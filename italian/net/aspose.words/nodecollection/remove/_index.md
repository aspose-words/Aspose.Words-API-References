---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo i nodi dal tuo documento con il metodo NodeCollection Remove, semplificando la gestione dei dati e migliorando le prestazioni.
type: docs
weight: 90
url: /it/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Rimuove il nodo dalla raccolta e dal documento.

```csharp
public void Remove(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo da rimuovere. |

## Esempi

Mostra come lavorare con un NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere testo al documento inserendo Runs tramite DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Ogni invocazione del metodo "Write" crea una nuova esecuzione,
// che poi appare nella RunCollection del Paragraph padre.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Possiamo anche inserire manualmente un nodo in RunCollection.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Accedi alle singole esecuzioni e rimuovile per rimuovere il relativo testo dal documento.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Guarda anche

* class [Node](../../node/)
* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
