---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompositeNode LastChild per accedere e manipolare facilmente l'ultimo nodo figlio, migliorando la gestione della struttura dei dati.
type: docs
weight: 50
url: /it/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Ottiene l'ultimo figlio del nodo.

```csharp
public Node LastChild { get; }
```

## Osservazioni

Se non c'è un ultimo nodo figlio, un`null` viene restituito.

## Esempi

Mostra come utilizzare i metodi Node e CompositeNode per rimuovere una sezione prima dell'ultima sezione nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Entrambe le sezioni sono gemelle l'una dell'altra.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Rimuove una sezione in base alla sua relazione di pari livello con un'altra sezione.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La sezione che abbiamo rimosso è la prima, lasciando nel documento solo la seconda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
