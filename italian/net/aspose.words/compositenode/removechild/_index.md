---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words per .NET
description: Gestisci senza sforzo il tuo CompositeNode con il metodo RemoveChild, progettato per semplificare la rimozione dei nodi per ottenere prestazioni ed efficienza migliorate.
type: docs
weight: 190
url: /it/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Rimuove il nodo figlio specificato.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| oldChild | T | Il nodo da rimuovere. |

### Valore di ritorno

Il nodo rimosso.

## Osservazioni

Il genitore di*oldChild* è impostato su`null` dopo la rimozione del nodo.

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
