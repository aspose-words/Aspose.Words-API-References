---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words per .NET
description: NodeCollection Insert metodo. Inserisce un nodo nella raccolta in corrispondenza dellindice specificato in C#.
type: docs
weight: 80
url: /it/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Inserisce un nodo nella raccolta in corrispondenza dell'indice specificato.

```csharp
public void Insert(int index, Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | L'indice in base zero del nodo. Gli indici negativi sono consentiti e indicano l'accesso dal fondo della lista. Ad esempio -1 significa l'ultimo nodo, -2 significa il penultimo e così via. |
| node | Node | Il nodo da inserire. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| NotSupportedException | IL[`NodeCollection`](../) è una collezione "profonda". |

## Osservazioni

Il nodo viene inserito come figlio nell'oggetto nodo da cui è stata creata la raccolta.

Se l'indice è uguale o maggiore di[`Count`](../count/), il nodo viene aggiunto alla fine della raccolta.

Se l'indice è negativo e il suo valore assoluto è maggiore di[`Count`](../count/), il nodo viene aggiunto alla fine della raccolta.

Se il nodo da inserire è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

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
