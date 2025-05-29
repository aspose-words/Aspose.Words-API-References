---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo InsertBefore di CompositeNode per inserire senza problemi i nodi prima dei nodi di riferimento, migliorando la gestione della struttura dei dati.
type: docs
weight: 160
url: /it/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore&lt;T&gt; method

Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato.

```csharp
public T InsertBefore<T>(T newChild, Node refChild)
    where T : Node
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newChild | T | IL[`Node`](../../node/) da inserire. |
| refChild | Node | IL[`Node`](../../node/) che è il nodo di riferimento. Il*newChild* è posizionato prima di questo nodo. |

### Valore di ritorno

Il nodo inserito.

## Osservazioni

Se*refChild* È`null` , inserti*newChild* alla fine dell'elenco dei nodi figlio.

Se il*newChild* è già presente nell'albero, prima viene rimosso.

Se il nodo inserito è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

## Esempi

Mostra come aggiungere, aggiornare ed eliminare nodi figlio nella raccolta di nodi figlio di un CompositeNode.

```csharp
Document doc = new Document();

// Per impostazione predefinita, un documento vuoto contiene un paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// I nodi compositi come il nostro paragrafo possono contenere altri nodi compositi e inline come figli.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea altri tre nodi di esecuzione.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Il corpo del documento non visualizzerà queste esecuzioni finché non le inseriremo in un nodo composito
// che a sua volta fa parte dell'albero dei nodi del documento, come abbiamo fatto con la prima esecuzione.
// Possiamo determinare dove si trova il contenuto di testo dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo nel paragrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserire la seconda esecuzione nel paragrafo che precede quella iniziale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserisce la terza esecuzione dopo quella iniziale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserisce la prima esecuzione all'inizio della raccolta di nodi figlio del paragrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Possiamo modificare il contenuto dell'esecuzione modificando ed eliminando i nodi figlio esistenti.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
