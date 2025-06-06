---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Scopri il metodo NodeCollection Add per aggiungere senza sforzo nodi alla tua raccolta, migliorando la gestione dei dati con facilità ed efficienza.
type: docs
weight: 30
url: /it/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Aggiunge un nodo alla fine della raccolta.

```csharp
public void Add(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo da aggiungere alla fine della raccolta. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| NotSupportedException | IL[`NodeCollection`](../) è una collezione "profonda". |

## Osservazioni

Il nodo viene inserito come figlio nell'oggetto nodo da cui è stata creata la raccolta.

Se il nodo inserito è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

## Esempi

Mostra come preparare un nuovo nodo di sezione per la modifica.

```csharp
Document doc = new Document();

// Un documento vuoto è composto da una sezione, che a sua volta ha un corpo, che a sua volta ha un paragrafo.
// Possiamo aggiungere contenuti a questo documento inserendo elementi come sequenze di testo, forme o tabelle nel paragrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Se aggiungiamo una nuova sezione come questa, non avrà un corpo né altri nodi figlio.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Esegui il metodo "EnsureMinimum" per aggiungere un corpo e un paragrafo a questa sezione per iniziare a modificarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [Node](../../node/)
* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
