---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words per .NET
description: DocumentBuilder MoveToBookmark metodo. Sposta il cursore su un segnalibro in C#.
type: docs
weight: 490
url: /it/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Sposta il cursore su un segnalibro.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Il nome del segnalibro su cui spostare il cursore. |

### Valore di ritorno

`VERO` se il segnalibro è stato trovato;`falso` Altrimenti.

## Osservazioni

Sposta il cursore in una posizione subito dopo l'inizio del segnalibro con il nome specificato.

Il confronto non fa distinzione tra maiuscole e minuscole. Se il segnalibro non è stato trovato,`falso` viene restituito is e il cursore non viene spostato.

L'inserimento di un nuovo testo non sostituisce il testo esistente del segnalibro.

Tieni presente che alcuni segnalibri nel documento sono assegnati a campi modulo. Passando a tale segnalibro e inserendo del testo lì, si inserisce il testo nel codice del campo modulo . Sebbene ciò non invaliderà il campo del modulo, il testo inserito non sarà visibile perché diventa parte del codice del campo.

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

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Sposta il cursore su un segnalibro con maggiore precisione.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | String | Il nome del segnalibro su cui spostare il cursore. |
| isStart | Boolean | Quando`VERO` , sposta il cursore all'inizio del segnalibro. Quando`falso`, sposta il cursore alla fine del segnalibro. |
| isAfter | Boolean | Quando`VERO` , sposta il cursore dopo la posizione iniziale o finale bookmark . Quando`falso`, sposta il cursore prima della posizione iniziale o finale bookmark . |

### Valore di ritorno

`VERO` se il segnalibro è stato trovato;`falso` Altrimenti.

## Osservazioni

Sposta il cursore in una posizione prima o dopo l'inizio o la fine del segnalibro.

Se la posizione desiderata non è a livello in linea, passa al paragrafo successivo.

Il confronto non fa distinzione tra maiuscole e minuscole. Se il segnalibro non è stato trovato,`falso` viene restituito is e il cursore non viene spostato.

## Esempi

Mostra come spostare il cursore del punto di inserimento del nodo di un generatore di documenti su un segnalibro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un segnalibro valido è costituito da un nodo BookmarkStart, un nodo BookmarkEnd con a
// nome del segnalibro corrispondente da qualche parte in seguito e contenuto racchiuso da tali nodi.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Esistono 4 modi per spostare il cursore del generatore di documenti su un segnalibro.
// Se ci troviamo tra i nodi BookmarkStart e BookmarkEnd, il cursore sarà all'interno del segnalibro.
// Ciò significa che qualsiasi testo aggiunto dal costruttore diventerà parte del segnalibro.
// 1 - All'esterno del segnalibro, davanti al nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - All'interno del segnalibro, subito dopo il nodo BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - All'interno del segnalibro, proprio di fronte al nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - All'esterno del segnalibro, dopo il nodo BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
