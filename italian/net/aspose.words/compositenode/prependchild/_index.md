---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words per .NET
description: CompositeNode PrependChild metodo. Aggiunge il nodo specificato allinizio dellelenco dei nodi secondari per questo nodo in C#.
type: docs
weight: 150
url: /it/net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild method

Aggiunge il nodo specificato all'inizio dell'elenco dei nodi secondari per questo nodo.

```csharp
public Node PrependChild(Node newChild)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newChild | Node | Il nodo da aggiungere. |

### Valore di ritorno

Il nodo ha aggiunto.

## Osservazioni

Se la*newChild* è già nell'albero, viene prima rimosso.

Se il nodo da inserire è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

## Esempi

Mostra come aggiungere, aggiornare ed eliminare i nodi figlio nella raccolta di figli di un CompositeNode.

```csharp
Document doc = new Document();

// Un documento vuoto, per impostazione predefinita, ha un paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// I nodi compositi come il nostro paragrafo possono contenere altri nodi compositi e in linea come figli.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea altri tre nodi di esecuzione.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Il corpo del documento non mostrerà queste esecuzioni finché non le inseriremo in un nodo composito
// quello stesso è una parte dell'albero dei nodi del documento, come abbiamo fatto con la prima esecuzione.
// Possiamo determinare dove si trova il contenuto del testo dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo del paragrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserisci la seconda sequenza nel paragrafo prima della sequenza iniziale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserisce la terza esecuzione dopo l'esecuzione iniziale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserisci la prima esecuzione all'inizio della raccolta dei nodi secondari del paragrafo.
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
