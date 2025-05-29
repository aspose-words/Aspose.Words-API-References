---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words per .NET
description: Scopri il metodo MoveTo di DocumentBuilder per navigare facilmente tra i nodi in linea e posizionare in modo efficiente il cursore alla fine dei paragrafi per una modifica fluida dei documenti.
type: docs
weight: 520
url: /it/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Sposta il cursore su un nodo in linea o alla fine di un paragrafo.

```csharp
public void MoveTo(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo deve essere un paragrafo o un figlio diretto di un paragrafo. |

## Osservazioni

Quandonodo è un nodo di livello inline, il cursore viene spostato su questo nodo e ulteriore contenuto verrà inserito prima di quel nodo.

Quandonodo è un[`Paragraph`](../../paragraph/)il cursore viene spostato alla fine del paragrafo e ulteriore contenuto verrà inserito appena prima dell'interruzione di paragrafo.

Quandonodo è un nodo a livello di blocco ma non un[`Paragraph`](../../paragraph/), il cursore viene spostato alla fine del primo paragrafo nel nodo a livello di blocco e ulteriore contenuto verrà inserito appena prima dell'interruzione di paragrafo.

## Esempi

Mostra come spostare la posizione del cursore di un DocumentBuilder su un nodo specificato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Il generatore di documenti ha un cursore, che funge da parte del documento
// dove il builder aggiunge nuovi nodi quando utilizziamo i suoi metodi di costruzione dei documenti.
// Questo cursore funziona allo stesso modo del cursore lampeggiante di Microsoft Word,
// e finisce sempre subito dopo ogni nodo appena inserito dal builder.
// Per aggiungere contenuto a una parte diversa del documento,
// possiamo spostare il cursore su un nodo diverso con il metodo "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Il cursore ora si trova davanti al nodo in cui lo abbiamo spostato.
// Aggiungendo una seconda esecuzione, questa verrà inserita davanti alla prima esecuzione.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Sposta il cursore alla fine del documento per continuare ad aggiungere testo alla fine come prima.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Mostra come spostare il cursore di un generatore di documenti su diversi nodi di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un segnalibro valido, un'entità costituita da nodi racchiusi da un nodo di inizio del segnalibro,
 // e un nodo finale segnalibro.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Il cursore del generatore di documenti è sempre davanti all'ultimo nodo che abbiamo aggiunto con esso.
// Se il cursore del builder si trova alla fine del documento, il suo nodo corrente sarà nullo.
// Il nodo precedente è il nodo finale del segnalibro che abbiamo aggiunto per ultimo.
// L'aggiunta di nuovi nodi con il builder li aggiungerà all'ultimo nodo.
Assert.Null(builder.CurrentNode);

// Se desideriamo modificare una parte diversa del documento con il builder,
// dovremo posizionare il cursore sul nodo che vogliamo modificare.
builder.MoveToBookmark("MyBookmark");

// Spostandolo in un segnalibro, verrà spostato al primo nodo all'interno dei nodi di inizio e fine del segnalibro, ovvero l'esecuzione inclusa.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Possiamo anche spostare il cursore su un singolo nodo in questo modo.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Possiamo utilizzare metodi specifici per spostarci all'inizio/fine di un documento.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Guarda anche

* class [Node](../../node/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
