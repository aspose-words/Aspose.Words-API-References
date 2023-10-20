---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: Aspose.Words per .NET
description: DocumentBuilder CurrentNode proprietà. Ottiene il nodo attualmente selezionato in questo DocumentBuilder in C#.
type: docs
weight: 40
url: /it/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Ottiene il nodo attualmente selezionato in questo DocumentBuilder.

```csharp
public Node CurrentNode { get; }
```

## Osservazioni

`CurrentNode` è un cursore di[`DocumentBuilder`](../) e indica a[`Node`](../../node/) che è un figlio diretto di a[`Paragraph`](../../paragraph/) . Qualsiasi operazione di inserimento eseguita utilizzando [`DocumentBuilder`](../) inserirà prima del`CurrentNode`.

Quando il paragrafo corrente è vuoto o il cursore è posizionato appena prima della fine di un paragrafo o di un tag di documento strutturato,`CurrentNode` ritorna`nullo`.

## Esempi

Mostra come spostare il cursore di un generatore di documenti su diversi nodi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un segnalibro valido, un'entità composta da nodi racchiusi da un nodo iniziale del segnalibro,
 // e un nodo finale del segnalibro.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Il cursore del generatore di documenti è sempre davanti al nodo che abbiamo aggiunto per ultimo.
// Se il cursore del builder è alla fine del documento, il suo nodo corrente sarà nullo.
// Il nodo precedente è il nodo finale del segnalibro aggiunto per ultimo.
// L'aggiunta di nuovi nodi con il builder li aggiungerà all'ultimo nodo.
Assert.Null(builder.CurrentNode);

// Se desideriamo modificare una parte diversa del documento con il builder,
// dovremo portare il cursore sul nodo che desideriamo modificare.
builder.MoveToBookmark("MyBookmark");

// Lo spostamento su un segnalibro lo sposterà sul primo nodo all'interno dei nodi iniziale e finale del segnalibro, la sequenza racchiusa.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Possiamo anche spostare il cursore su un singolo nodo come questo.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Possiamo usare metodi specifici per spostarci all'inizio/fine di un documento.
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
