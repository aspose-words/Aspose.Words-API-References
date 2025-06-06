---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Scopri la proprietà Documento Nodo, accedi senza sforzo al documento collegato al tuo nodo per una gestione dei dati fluida e una maggiore produttività.
type: docs
weight: 20
url: /it/net/aspose.words/node/document/
---
## Node.Document property

Ottiene il documento a cui appartiene questo nodo.

```csharp
public virtual DocumentBase Document { get; }
```

## Osservazioni

Il nodo appartiene sempre a un documento, anche se è stato appena creato e non ancora aggiunto all'albero, oppure se è stato rimosso dall'albero.

## Esempi

Mostra come creare un nodo e impostare il documento proprietario.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Non abbiamo ancora aggiunto questo paragrafo come figlio a nessun nodo composito.
Assert.IsNull(para.ParentNode);

// Se un nodo è un tipo di nodo figlio appropriato di un altro nodo composito,
// possiamo collegarlo come figlio solo se entrambi i nodi hanno lo stesso documento proprietario.
// Il documento proprietario è il documento che abbiamo passato al costruttore del nodo.
// Non abbiamo allegato questo paragrafo al documento, quindi il documento non ne contiene il testo.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Poiché il documento è proprietario di questo paragrafo, possiamo applicare uno dei suoi stili al contenuto del paragrafo.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Aggiungi questo nodo al documento e verificane il contenuto.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
