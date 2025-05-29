---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words per .NET
description: Inserisci senza sforzo i nodi nella tua NodeCollection a qualsiasi indice con il nostro metodo di inserimento semplificato. Migliora la tua gestione dei dati oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Inserisce un nodo nella raccolta all'indice specificato.

```csharp
public void Insert(int index, Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Indice basato su zero del nodo. Gli indici negativi sono consentiti e indicano l'accesso dalla parte posteriore dell'elenco. Ad esempio -1 indica l'ultimo nodo, -2 indica il penultimo e così via. |
| node | Node | Il nodo da inserire. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| NotSupportedException | IL[`NodeCollection`](../) è una collezione "profonda". |

## Osservazioni

Il nodo viene inserito come figlio nell'oggetto nodo da cui è stata creata la raccolta.

Se l'indice è uguale o maggiore di[`Count`](../count/), il nodo viene aggiunto alla fine della raccolta.

Se l'indice è negativo e il suo valore assoluto è maggiore di[`Count`](../count/), il nodo viene aggiunto alla fine della raccolta.

Se il nodo inserito è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

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
