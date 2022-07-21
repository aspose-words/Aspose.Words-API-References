---
title: MoveToBookmark
second_title: Aspose.Words per .NET API Reference
description: Sposta il cursore su un segnalibro.
type: docs
weight: 470
url: /it/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

Sposta il cursore su un segnalibro.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Il nome del segnalibro su cui spostare il cursore. |

### Valore di ritorno

True se il segnalibro è stato trovato; falso altrimenti.

### Osservazioni

Sposta il cursore in una posizione subito dopo l'inizio del segnalibro con il nome specificato.

Il confronto non fa distinzione tra maiuscole e minuscole. Se il segnalibro non è stato trovato, viene restituito false e il cursore non viene spostato.

L'inserimento di nuovo testo non sostituisce il testo esistente del segnalibro.

Si noti che alcuni segnalibri nel documento sono assegnati ai campi modulo. Spostandosi su un segnalibro di questo tipo e inserendo del testo in esso si inserisce il testo nel codice del campo del modulo . Anche se ciò non invaliderà il campo del modulo, il testo inserito non sarà visibile perché diventa parte del codice del campo.

### Esempi

Mostra come spostare il cursore di un generatore di documenti su nodi diversi in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un segnalibro valido, un'entità composta da nodi racchiusi da un nodo di inizio segnalibro,
 // e un nodo finale del segnalibro.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Il cursore del generatore di documenti è sempre davanti al nodo che abbiamo aggiunto per ultimo con esso.
// Se il cursore del builder si trova alla fine del documento, il suo nodo corrente sarà nullo.
// Il nodo precedente è il nodo finale del segnalibro che abbiamo aggiunto per ultimo.
// L'aggiunta di nuovi nodi con il builder li aggiungerà all'ultimo nodo.
Assert.Null(builder.CurrentNode);

// Se desideriamo modificare una parte diversa del documento con il builder,
// dovremo portare il cursore sul nodo che desideriamo modificare.
builder.MoveToBookmark("MyBookmark");

// Lo spostamento in un segnalibro lo sposterà sul primo nodo all'interno dei nodi di inizio e fine del segnalibro, la corsa racchiusa.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Possiamo anche spostare il cursore su un singolo nodo come questo.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Possiamo usare metodi specifici per spostarci all'inizio/alla fine di un documento.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Guarda anche

* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

Sposta il cursore su un segnalibro con maggiore precisione.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Il nome del segnalibro su cui spostare il cursore. |
| isStart | Boolean | Se vero, sposta il cursore all'inizio del segnalibro. Se falso, sposta il cursore alla fine del segnalibro. |
| isAfter | Boolean | Se true, sposta il cursore dopo la posizione iniziale o finale del bookmark . Se false, sposta il cursore prima della posizione iniziale o finale del bookmark . |

### Valore di ritorno

True se il segnalibro è stato trovato; falso altrimenti.

### Osservazioni

Sposta il cursore in una posizione prima o dopo l'inizio o la fine del segnalibro.

Se la posizione desiderata non è in linea, passa al paragrafo successivo.

Il confronto non fa distinzione tra maiuscole e minuscole. Se il segnalibro non è stato trovato, viene restituito false e il cursore non viene spostato.

### Esempi

Mostra come spostare il cursore del punto di inserimento del nodo di un generatore di documenti su un segnalibro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un segnalibro valido è costituito da un nodo BookmarkStart, un nodo BookmarkEnd con a
// il nome del segnalibro corrispondente da qualche parte dopo e il contenuto racchiuso da quei nodi.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Esistono 4 modi per spostare il cursore di un generatore di documenti su un segnalibro.
// Se ci troviamo tra i nodi BookmarkStart e BookmarkEnd, il cursore sarà all'interno del segnalibro.
// Ciò significa che qualsiasi testo aggiunto dal builder diventerà parte del segnalibro.
// 1 - Al di fuori del segnalibro, davanti al nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - All'interno del segnalibro, subito dopo il nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - All'interno del segnalibro, proprio davanti al nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Al di fuori del segnalibro, dopo il nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Guarda anche

* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
