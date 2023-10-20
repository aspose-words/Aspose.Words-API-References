---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words per .NET
description: NodeCollection Contains metodo. Determina se un nodo è nella raccolta in C#.
type: docs
weight: 50
url: /it/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Determina se un nodo è nella raccolta.

```csharp
public bool Contains(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo da individuare. |

### Valore di ritorno

`VERO` se l'articolo si trova nella raccolta; Altrimenti,`falso`.

## Osservazioni

Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a[`Count`](../count/).

## Esempi

Mostra come lavorare con una NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi testo al documento inserendo Runs utilizzando un DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Ogni invocazione del metodo "Write" crea una nuova Run,
// che verrà quindi visualizzato nella RunCollection del paragrafo principale.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Possiamo anche inserire manualmente un nodo nella RunCollection.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Accedi alle singole esecuzioni e rimuovile per rimuovere il testo dal documento.
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
