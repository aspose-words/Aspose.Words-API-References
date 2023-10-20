---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words per .NET
description: Node ParentNode proprietà. Ottiene il genitore immediato di questo nodo in C#.
type: docs
weight: 60
url: /it/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Ottiene il genitore immediato di questo nodo.

```csharp
public CompositeNode ParentNode { get; }
```

## Osservazioni

Se un nodo è stato appena creato e non ancora aggiunto all'albero, o se è stato rimosso dall'albero, il genitore è`nullo`.

## Esempi

Mostra come accedere al nodo genitore di un nodo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aggiunge un nodo Esegui figlio al primo paragrafo del documento.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Il paragrafo è il nodo genitore del nodo di esecuzione. Possiamo tracciare questo lignaggio
// fino al nodo del documento, che è la radice dell'albero dei nodi del documento.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Mostra come creare un nodo e impostare il documento proprietario.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Non abbiamo ancora aggiunto questo paragrafo come figlio a nessun nodo composito.
Assert.IsNull(para.ParentNode);

// Se un nodo è un tipo di nodo figlio appropriato di un altro nodo composito,
// possiamo allegarlo come figlio solo se entrambi i nodi hanno lo stesso documento proprietario.
// Il documento proprietario è il documento che abbiamo passato al costruttore del nodo.
// Non abbiamo allegato questo paragrafo al documento, quindi il documento non contiene il suo testo.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Poiché il documento possiede questo paragrafo, possiamo applicare uno dei suoi stili al contenuto del paragrafo.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Aggiungi questo nodo al documento, quindi verificane il contenuto.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
