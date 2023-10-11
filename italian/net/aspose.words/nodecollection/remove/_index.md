---
title: NodeCollection.Remove
second_title: Aspose.Words per .NET API Reference
description: NodeCollection metodo. Rimuove il nodo dalla raccolta e dal documento.
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

### Esempi

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
* spazio dei nomi [Aspose.Words](../../nodecollection/)
* assemblea [Aspose.Words](../../../)


