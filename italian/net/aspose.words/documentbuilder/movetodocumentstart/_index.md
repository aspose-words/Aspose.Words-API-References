---
title: DocumentBuilder.MoveToDocumentStart
linktitle: MoveToDocumentStart
articleTitle: MoveToDocumentStart
second_title: Aspose.Words per .NET
description: Scopri il metodo MoveToDocumentStart di DocumentBuilder per passare senza sforzo all'inizio del documento, migliorando l'efficienza della tua modifica.
type: docs
weight: 560
url: /it/net/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder.MoveToDocumentStart method

Sposta il cursore all'inizio del documento.

```csharp
public void MoveToDocumentStart()
```

## Esempi

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

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
